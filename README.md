# Frontend Mentor - Stats preview card component solution

## Hello everyone! 👋

Here I'm writing my learning process in this challenge.

1. I had trouble with creating a fitted image in flexbox layout and at the same time this would also be responsive. I solved it using the following code:

```css
.image-content {
	width: 100%;
}

.image-content img {
	display: block;
	width: 100%;
	height: 100%;
	object-fit: cover;
	border-radius: 0 0.625rem 0.625rem 0;
}
```

2. Coloring the picture was also not easy, and it seems that I still haven't hit the specific color according to the reference design. There was some ways to color the image, so I choose the following code, because it removes the need to use background images which make trouble in mobile view, and adding more div as overlay element:

```css
.image-content {
	width: 100%;
	position: relative;
}

.image-content::after {
	content: '';
	position: absolute;
	top: 0;
	left: 0;
	width: 100%;
	height: 100%;
	background: var(--accent);
	mix-blend-mode: overlay;
	border-radius: 0 0.625rem 0.625rem 0;
}

.image-content img {
	display: block;
	width: 100%;
	height: 100%;
	object-fit: cover;
	border-radius: 0 0.625rem 0.625rem 0;
	filter: brightness(.5);
}
```
You can view the summbited solution here [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62)