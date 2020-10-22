# UIB Basic Layout

## Browser defaults

The browser set some default styles, so even without any CSS applyed we can see the document structure and we can tell a headline apart from a paragraph.

Different browsers will have diffent defaults, which might cause unpredictable results for us.

There are 2 popular solutions:

* [Reset.css](https://meyerweb.com/eric/tools/css/reset/)

    It will remove all default styles, and we will no longer be able to tell elements apart. It gives you a clean slate.

* [Normalize.css]( https://necolas.github.io/normalize.css/ )

    It tries to normalize the styles across different browsers.

You can include these libraries (pick one) in the `head` of the document. Make sure they go above your custom styles.

You can also add your own custom reset.

## Basic responsive layout

We could make use of `margin: 0 auto;` to center an entire block on the page.
This block should have a width that is less than the full width of the browser or the parent, otherwise we will not see the effect.

To set the width of this container we could use a `%` or `vw`, but both are relative units and on smaller screens the content would be too narrow.

So instead we could use `px`, which is absolute unit. The issue will be on smaller screens - when the width we set is larger than the device width, which will cause a horizontal scrollbar, something we want to avoid.

To fix this, we can use instead of the `width` property, the `max-width` in combination with a px value.
We could set the sizing of the container like: `max-width: 900px;`. This mean our container will expand to 100% of the parent (given that it is a block level element) but only until it reaches the specified `max-width` of `900px`. After it reaches this size it will be centered on the screen due to the `margin: 0 auto;`. 

Last we need to add some padding, so the content does not stick to the edge of the browser on smaller screens.

## In Page Navigation

- add `id` to the section you want to be able to navigate to
- use this `id` as the `href` of an anchor tag preceeded with a `#`, like `href="#team"`

## Pretty URLs

- use an `index.html` file inside a folder
- include the same CSS file in the head of the document, to ensure same visual appearance

## Folder structure

Make sure you keep your project organized and group files in folders. This is our project structure:

```bash
    .
    ├── about
    │   └── index.html
    ├── images
    │   └── panda.png
    ├── lib
    │   ├── normalize.css
    │   └── reset.css
    ├── styles
    │   └── main.css
    ├── README.md
    └── index.html
```