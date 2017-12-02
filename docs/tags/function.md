# @function

## 内容列表 🕊️

* [同义词](#synonyms "Synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="synonyms">同义词</span>

* @func
* @method

## <span id="syntax">语法</span>

`@function [<FunctionName>]`

## <span id="overview">概述</span>

`@function` 标签将一个对象标记为函数，即使在解析器看来这个对象并不是一个函数。该标签将文档注释中的 [@kind](https://ninjiahub.github.io/JSDoc/docs/tags/kind "tag @kind") 设置为 **`function`**。

## <span id="examples">示例</span>

**使用 @function 标记函数**

```javascript
/** @function */
var paginate = paginateFactory(pages);
```

如果没有 `@function` 标签，`paginate` 将会被标记为一个普通对象([@memeber](https://ninjiahub.github.io/JSDoc/docs/tags/memeber "tag @memeber"))，因为仅检查这行代码并不能确定在代码运行时 **paginate** 被赋予的值的类型。

**使用带 functionName 的 @function 标签**

```javascript
/** @function myFunction */

// the above is the same as:
/** @function
 * @name myFunction */
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @function](http://usejsdoc.org/tags-function.html "tag function")。

如有版权问题请联系译者。

侵删。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>