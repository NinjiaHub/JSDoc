# @constant

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="Synonyms">同义词</span>

`@const`

## <span id="syntax">语法</span>

`@constant [<type> <name>]`

## <span id="overview">概述</span>

@constant 标签用来表示一个文档注释属于一个常量标识符。

## <span id="examples">示例</span>

在这个例子中我们给字符串常量添加文档注释。虽然代码中使用了关键字 `const`，但这并不是 JSDoc 的必须条件。如果你的 JavaScript 运行环境暂不支持常量声明，使用 `var` 关键字声明变量也能正常工作。

**表示红色的字符串常量**

```javascript
/** @constant
    @type {string}
    @default
*/
const RED = 'FF0000';

/** @constant {number} */
var ONE = 1;
```

注意上面的例子使用 `@type` 标签提供了类型，该标签是可选的。上面的例子也使用了可选的 `@default` 标签，这会将赋值给常量标识符的值(比如 '#FF0000')添加到文档中。

## <span id="related">相关链接</span>

* [@default](https://ninjiahub.github.io/JSDoc/docs/tags/default "tag @default")
* [@type](https://ninjiahub.github.io/JSDoc/docs/tags/type "tag @type")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @constant](http://usejsdoc.org/tags-constant.html "tag @constant")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>