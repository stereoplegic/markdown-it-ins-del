# markdown-it-ins-del

> `<ins>` and `<del>` tag plugin for [markdown-it](https://github.com/markdown-it/markdown-it) markdown parser.
Also enables attribution of editor

__v0.1.+ requires `markdown-it` v4.+, see changelog.__

`++insert++[WZ]` => `<ins>insert</ins><sup>WZ</sup>`
`~~delete~~[WZ]` => `<del>delete</del><sup>WZ</sup>`

Markup uses the same conditions as CommonMark [emphasis](http://spec.commonmark.org/0.15/#emphasis-and-strong-emphasis).


## Install

node.js, browser:

```bash
npm install markdown-it-ins-del --save
bower install markdown-it-ins-del --save
```

## Use

```js
var md = require('markdown-it')()
            .use(require('markdown-it-ins-del'))
            .disable('strikethrough');

md.render('++insert++[WZ]') // => '<p><ins>inserted</ins><sup>WZ</sup></p>'
md.render('++insert++[WZ]') // => '<p><del>delete</del><sup>WZ</sup></p>'
```

Disable the 'strikethrough' module in Markdown-it.

_Differences in browser._ If you load script directly into the page, without
package system, module will add itself globally as `window.markdownitIns`.


## License

[MIT](https://github.com/markdown-it/markdown-it-ins-del-attributable/blob/master/LICENSE)
