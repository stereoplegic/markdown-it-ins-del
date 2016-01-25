# markdown-it-ins-del

> `<ins>` and `<del>` tag plugin for [markdown-it](https://github.com/markdown-it/markdown-it) markdown parser with
editor attributions. Forked from https://github.com/WenTingZhu/markdown-it-ins-del, but allows use of markdown-it's native strikethrough (`<s>` tag) via `~~`, instead using `!!` for `<del>` tags. While `--` seems like it would make more sense (and my first choice), markdown-it's build in typography plugin already uses `--` for en dashes.

__v0.1.+ requires `markdown-it` v4.+, see changelog.__

`++insert++[WZ]` => `<ins>insert</ins><sup>WZ</sup>`

`!!delete!![WZ]` => `<del>delete</del><sup>WZ</sup>`

Markup uses the same conditions as CommonMark [emphasis](http://spec.commonmark.org/0.15/#emphasis-and-strong-emphasis).


## Install

node.js, browser:

```bash
npm install git://github.com/stereoplegic/markdown-it-ins-del.git --save
bower install git://github.com/stereoplegic/markdown-it-ins-del.git --save
```

## Use

```js
var md = require('markdown-it')()
            .use(require('markdown-it-ins-del'));

md.render('++insert++[WZ]') // => '<p><ins>insert</ins><sup>WZ</sup></p>'
md.render('!!delete!![WZ]') // => '<p><del>delete</del><sup>WZ</sup></p>'
```

<del>Disable the 'strikethrough' module in Markdown-it.</del>
<ins>This fork allows markdown-it's strikethrough module to use ~~ for &lt;s&gt; tags, instead using !! and producing &lt;del&gt; tags.</ins>

_Differences in browser._ If you load script directly into the page, without
package system, module will add itself globally as `window.markdownitIns`.


## License

[MIT](https://github.com/stereoplegic/markdown-it-ins-del/blob/master/LICENSE)
