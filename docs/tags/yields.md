# @yields

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="Synonyms">同义词</span>

`@yield`

## <span id="syntax">语法</span>

`@yields [{type}] [description]`

## <span id="overview">概述</span>

`@yields` 标签用来给 **generator** 函数的生成值添加文档注释。该标签在 **JSDoc 3.5.0** 及其之后的版本中可用。

如果标记普通方法，请使用 [@returns](https://ninjiahub.github.io/JSDoc/docs/tags/returns "tag @returns") 标签。

## <span id="examples">示例</span>

**@yields 标签中使用 [{type}]**

```javascript
/**
 * Generate the Fibonacci sequence of numbers.
 *
 * @yields {number}
 */
function* fibonacci() {}
```

**@yields 标签中使用 [{type}] 和 [description]**

```javascript
/**
 * Generate the Fibonacci sequence of numbers.
 *
 * @yields {number} The next number in the Fibonacci sequence.
 */
function* fibonacci() {}
```

## <span id="related">相关链接</span>

* [@returns](https://ninjiahub.github.io/JSDoc/docs/tags/returns "tag @returns")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @yields](http://usejsdoc.org/tags-yields.html "tag @yields")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>