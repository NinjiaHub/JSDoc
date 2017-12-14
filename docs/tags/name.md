# @name

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@name <namePath>`

## <span id="overview">概述</span>

`@name` 标签强制 JSDoc 将当前注释中的剩余注释与给定的名字关联在一起，并且忽略其余代码。这个标签最好以“虚拟注释”的方式应用于代码中不易读的标识符上，例如运行时生成的方法。

当使用 `@name` 标签时，必须提供额外的标签告诉 JSDoc 更多信息，比如当前标识符的类型、该标识符是不是其他标识符的成员等。如果不提供这些信息，生成的标识符文档可能是不正确的。

**警告：** 通过使用 `@name` 标签，你告诉 JSDoc 忽略代码上下文并且单独处理你书写的 JSDoc 文档注释。在很多情况下，最好使用 [@alias](https://ninjiahub.github.io/JSDoc/docs/tags/alias "tag @alias") 标签来代替 `@name` 标签，该标签可以修改标识符在文档中的名字，并且可以提供其他信息。

## <span id="examples">示例</span>

下面的例子展示了如何使用 `@name` 标签给不能被 JSDoc 正常识别的函数添加文档注释。

**使用 @name 标签**

```javascript
/**
 * @name highlightSearchTerm
 * @function
 * @global
 * @param {string} term - The search term to highlight.
 */
eval("window.highlightSearchTerm = function(term) {};")
```

## <span id="related">相关链接</span>

* [Using namepaths with JSDoc 3](https://ninjiahub.github.io/JSDoc/docs/start/about-namepaths "start Using namepaths with JSDoc 3")
* [@alias](https://ninjiahub.github.io/JSDoc/docs/tags/alias "tag @alias")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @name](http://usejsdoc.org/tags-name.html "tag @name")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>