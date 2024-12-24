# Front-end Style Guide

## Layout

The designs were created to the following widths:

- Mobile: 375px
- Desktop: 1440px

> 💡 These are just the design sizes. Ensure content is responsive and meets WCAG requirements by testing the full range of screen sizes from 320px to large screens.

## Colors

### Primary

- Dark cyan: hsl(158, 36%, 37%)
- Cream: hsl(30, 38%, 92%)

### Neutral

- Very dark blue: hsl(212, 21%, 14%)
- Dark grayish blue: hsl(228, 12%, 48%)
- White: hsl(0, 0%, 100%)

## Typography

### Body Copy

- Font size (paragraph): 14px

### Font

- Family: [Montserrat](https://fonts.google.com/specimen/Montserrat)
- Weights: 500, 700

- Family: [Fraunces](https://fonts.google.com/specimen/Fraunces)
- Weights: 700

> 💎 [Upgrade to Pro](https://www.frontendmentor.io/pro?ref=style-guide) for design file access to see all design details and get hands-on experience using a professional workflow with tools like Figma.

---

/_ 1. Use a more-intuitive box-sizing model _/
_,
_::before,
\*::after {
box-sizing: border-box;
margin: 0;
padding: 0;

}

/_ 5. Improve media defaults _/
img,
picture,
video,
canvas,
svg {
display: block;
max-width: 100%;
}

/_ 6. Inherit fonts for form controls _/
input,
button,
textarea,
select {
font: inherit;
}

/_ 7. Avoid text overflows _/
p,
h1,
h2,
h3,
h4,
h5,
h6 {
overflow-wrap: break-word;
}

/_ 8. Improve line wrapping _/
p {
text-wrap: pretty;
}

h1,
h2,
h3,
h4,
h5,
h6 {
text-wrap: balance;
}

:root {
--clr--dark-cyan: hsl(158, 36%, 37%);
--clr--bg-cream: hsl(30, 38%, 92%);
--clr--dark-blue: hsl(212, 21%, 14%);
--clr--gray-blue: hsl(228, 12%, 48%);
--clr--slate-white: hsl(0, 0%, 100%);

}

body {
background-color: var(--clr--bg-cream);
font-size: 0.875rem;
font-weight: 500;
color: var(--clr--gray-blue);
font-family: "Montserrat", serif;
display: flex;
justify-content: center;
align-items: center;
min-height: 100vh;
border: 1px solid red;

}

/_ typography _/
.product-logo {
font-size: 0.9rem;
font-weight: 500;
text-transform: uppercase;
letter-spacing: .3em;
}

.product-tagline {
color: var(--clr--dark-blue);
font-family: "Fraunces", serif;
font-size: 1.8rem;
}

.product-body {
letter-spacing: 0.03em
}

.final-price {
font-family: "Fraunces", serif;
font-size: 2rem;
color: var(--clr--dark-cyan);
font-weight: 700;
}

.mrp-price {
text-decoration: line-through;
}

.add-cart-btn {
font-weight: 700;
color: var(--clr--slate-white);
text-decoration: none;
}

.add-cart-wrapper:hover,
.add-cart-wrapper:focus {
background-color: hsl(158, 50%, 30%);
transition: background-color 0.3s ease-in-out;
cursor: pointer;

}

/_ layout _/

.product-container {
width: 90%;
max-width: 350px;
background-color: var(--clr--slate-white);
display: flex;
flex-direction: column;

}

.product-content {
padding: 2em 1em;
display: flex;
flex-direction: column;
justify-content: space-between;
gap: 1rem
}

.product-price-wrapper {

    display: flex;
    gap: 1rem;
    align-items: center;

}

.add-cart-wrapper {
background-color: var(--clr--dark-cyan);
display: flex;
align-items: center;
justify-content: center;
gap: 0.7rem;
padding: 1em 3em;
border-radius: 0.7em;
}

@media (min-width:650px) {

    .product-container {
        flex-direction: row;
        max-width: 650px;
        gap: 1rem;
        border-radius: 0.5em
    }

    @media (min-width:1400px) {

        .product-container {
            flex-direction: row;
            max-width: 850px;
            gap: 1rem;
            border-radius: 0.5em
        }

        picture {
            border-top-left-radius: 0.5em;
            border-bottom-left-radius: 0.5em;
        }

        .product-content {
            gap: 2rem;
            justify-content: center;

        }

    }

}
