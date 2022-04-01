# Node使う版

## ソース/実行結果

``` javascript
const jsdom = require('jsdom');
const { JSDOM } = jsdom;
const dom = new JSDOM(`<html><body><div id="aaa">AAA<div></body></html>`);
const { document } = dom.window;
const jquery = require('jquery');
const $ = jquery(dom.window);

console.log($("#aaa"));
console.log($("#aaa").text());
console.log($("#aaa")[0].id);
```

``` sh
npm install
npm start
```

``` txt
jQuery { '0': HTMLDivElement {}, length: 1 }
AAA
aaa
```

## 参考

[NodeJSでjQueryを使う:Qiita](https://qiita.com/gitcho/items/251c66947c0b1d5b5523)