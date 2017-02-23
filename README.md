# jsdoc-rtd
A readthedocs-style themed jsdoc template. Forked from [TUI JSDoc Template](https://github.com/nhnent/tui.jsdoc-template).

![Example](https://cloud.githubusercontent.com/assets/213060/23259167/0dd22ca4-f9cc-11e6-9d5e-3ed926c85296.png)
## install
```
npm i -D jsdoc-rtd
```

## Feature
jsdoc-rtd inherits the following features from TUI JSDoc template:

* Navigation - AutoComplete Searchbox
* Navigation - Members / Methods / Events
* Navigation - API / Examples(Tutorials) Tab
* Navigation - Resize
* Examples - HTML/JS source tab in example page

## Configuration
([*jsdoc page - configuration*](http://usejsdoc.org/about-configuring-jsdoc.html#incorporating-command-line-options-into-the-configuration-file))

### Template
```
"opts": {
    "template": "node_modules/jsdoc-rtd"
}
```

### Logo Image
```
"templates": {
    "logo": {
        "url": "http://url.to/image.png",
        "width": "72px",
        "height": "60px"
    }
}
```

### Page Title
```
"templates": {
    "name": "jsdoc template"
}
```

### FooterText
```
"templates": {
    "footerText": "some text"
}
```

### Use collapsible api list
*Default: `true`*
```
"templates": {
    "useCollapsibles": ture
}
```

### Tab Names
```
"templates": {
    "tabNames": {
        "api": "API",
        "tutorials": "Examples"
    }
}
```

`api` defaults to the value `API` and `tutorials` defaults to the value `Examples`.

### Custom Styles
With a folder structure like this:
```
static
└── styles
    └── custom.css
    └── another.css
```
And a config like this:
```js
"templates": {
    "default": {
        "staticFiles": {
            "include": ["static/"]
        }
    },
    "css": [
        "styles/custom.css",
        "styles/another.css",
        "http://example.com/remote.css"
    ]
}
```

`styles/custom.css`, `styles/another.css`, and `remote.css` get included in the layout.
`default.staticFiles` is the build-in jsdoc way of copying extra files.

<br>
## Expose the html/js code to example page
If `script` or `div` elements have `code-js` or `code-html` class, expose their innerHTML.

1. innerHTML of `script.code-js` tag
2. innerHTML of `div.code-html` tag

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>example</title>
</head>
<body>
    <div class="code-html">
        <h3> Base Example </h3>
        <p> Hello world </p>
    </div>

    <script class="code-js">
        console.log('hello world');
    </script>
</body>
</html>

```
