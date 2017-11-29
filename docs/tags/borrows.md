# @borrows

## 内容列表 🕊️

* [概述](#overview "overview")
* [语法](#syntax "syntax")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@borrows <that namepath> as <this namepath>`

## <span id="overview">概述</span>

`@borrows` 标签允许引用给另外一个标识添加的文档注释到当前的注释中。

如果有很多地方或者很多方式引用同一个方法，又不想多次重复书写相同的文档注释时，使用 `@borrows` 标签会是一个不错的选择。

## <span id="examples">示例</span>

下面的例子中，`trstr` 方法的文档注释已经存在了，为了不重复书写相同的文档注释，在 `util.trim` 的文档注释中可以通过 `@borrows` 标签引用 `trstr` 方法的文档注释，注意要使用别名 (**as trim**)。

**util.trim 复用 trstr 方法的文档注释**

```javascript
/**
 * @namespace
 * @borrows trstr as trim
 */
var util = {
    trim: trstr
};

/**
 * Remove whitespace from around a string.
 * @param {string} str
 */
function trstr(str) {
}
```
## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - Using namepaths with JSDoc 3](http://usejsdoc.org/about-namepaths.html "namepaths")。

如有版权问题请联系译者。

侵删。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>