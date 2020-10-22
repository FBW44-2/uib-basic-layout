# UIB Basic Layout

## Browser defaults

The browser set some default styles, so even without any CSS applyed we can see the document structure and we can tell a headline apart from a paragraph.

Different browsers will have diffent defaults, which might cause unpredictable results for us.

There are 2 popular solutions:

* [Reset.css](https://meyerweb.com/eric/tools/css/reset/)

    It will remove all default styles, and we will no longer be able to tell elements apart. It gives you a clean slate.

* [normalize.css]( https://necolas.github.io/normalize.css/ )

    It tries to normalize the styles across different browsers.

You can include these libraries (pick one) in the `head` of the document. Make sure they go above your custom styles.

You can also add your own custom reset.

## In Page Navigation

- add `id` to the section you want to be able to navigate to
- use this `id` as the `href` of an anchor tag preceeded with a `#`, like `href="#team"`

## Pretty URLs

- use an `index.html` file inside a folder
- include the same CSS file in the head of the document, to ensure same visual appearance