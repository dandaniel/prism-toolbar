## 'View source' and 'Copy to clipboard' for [prism.js](http://prismjs.com)

This plugin is made for [fadeit OLS front-end style guide](https://github.com/fadeit/ols-styleguide), but should work fine for Prism in general (with some additional styling). In ordet to match the style in the screenshots below, check out [this stylesheet](https://github.com/fadeit/ols-styleguide/blob/master/assets/this-styleguide.less#L100-L164) (LESS) and [this script](https://github.com/fadeit/ols-styleguide/blob/master/assets/this-styleguide.js#L1-L27) for collapsing/expanding the code. Maybe someday I will merge them if somebody finds it useful.

<img src="http://danmind.ru/tmp/prism-toolbar-collapsed.png" alt="Prism Toolbar Collapsed" border="2"/><br/>
<img src="http://danmind.ru/tmp/prism-toolbar-expanded.png" alt="Prism Toolbar Expanded" border="2"/><br/>

Under the hood, this plugin uses [Zeroclipboard](http://zeroclipboard.org) (V2), which in turn uses Flash to allow copying to clipboard. Apparently, this is the only way to do it in a consistent manner. If you are not sure about it (I wasn't), you should know that [Github](https://github.com/blog/1365-a-more-transparent-clipboard-button) is also using it.

### Getting started
Include the CSS in the `<head>` of your document and the scripts before the closing `</body>` tag.

```html
<head>
...
  <link rel="stylesheet" href="assets/prism-toolbar.css">
</head>
<body>
  ...
  <script src="./assets/ZeroClipboard.min.js"></script>
  <script src="./assets/prism-toolbar.js"></script>
</body>
```

Add the class `code-toolbar` to a `pre` element to display the toolbar.

```html
<pre class="code-toolbar">
  <code>
    ...
  </code>
</pre>
```


### Gotchas
Remember to run it on a server.

### Credits
Credits to Philip Lawrence, developing the toolbar for the first time at [misterphilip.com](http://dev.misterphilip.com/prism/plugins/toolbar/)