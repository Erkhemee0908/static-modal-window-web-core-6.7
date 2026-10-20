# Modal Window Demo

A static HTML and CSS page that shows a modal window always displayed above the page content. No JavaScript and no external libraries.

## Files

* `index.html`: page structure (header, main, section, and the modal)
* `style.css`: styles, including the modal styles (the stylesheet linked in `index.html`)

## How it works

* `.modal` is fixed to the viewport (`top`, `left`, `right`, `bottom` set to 0) and uses flexbox to center `.modal-content`.
* `.modal-backdrop` covers the screen with `rgba(0, 0, 0, 0.5)`.
* `.modal-content` has rounded corners, a shadow, and a max width with padding so it fits mobile screens.

## Z-index layers

| Element | Position | Z-index |
| --- | --- | --- |
| Main content | relative | 1 |
| `.modal` | fixed | 1000 |
| `.modal-backdrop` | absolute | 1 |
| `.modal-content` | relative | 2 |

The modal sits at the root level of `<body>`, so no parent creates a stacking context that could trap it.

## Run

Open `index.html` in any browser.
