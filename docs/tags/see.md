# @see

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

* `@see <namepath>`
* `@see <text>`

## <span id="overview">概述</span>

`@see` 标签允许引用别的标识符或者已经注释过的源。可以提供一个标识符的命名路由或者自由格式的文字。如果使用命名路由，JSDoc 的默认模版会自动将命名路由转换为链接。

## <span id="examples">示例</span>

**使用 @see 标签**

```javascript
/**
 * Both of these will link to the bar function
 * @see bar
 */
function foo() {}

// Use the inline {@link} tag to include a link within a free-form description.
/**
 * @see {@link foo} for further information.
 * @see {@link http://github.com|GitHub}
 */
function bar() {}
```
## <span id="related">相关链接</span>

* [{@link}](https://ninjiahub.github.io/JSDoc/docs/tags/inline-link "tag @inline-link")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @see](http://usejsdoc.org/tags-see.html "tag see")。

如有版权问题请联系译者。

侵删。

内容如有错误或者不恰当的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>