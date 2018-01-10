# @async

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="syntax">语法</span>

`@async`

## <span id="overview">概述</span>

`@async` 标签表示一个方法是 [异步](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)的，这意味着该方法是使用 `async function foo() {}` 这种语法声明的。不要将此标签用于其他类型的异步方法，比如使用回调的异步。该标签在 JSDoc 3.5 及其之后的版本中可用。

一般情况下不需要使用该标签，因为 JSDoc 会自动检测异步方法并在生成的文档中标记出来。然而，如果你为一个不出现在代码中的异步方法写虚拟注释时，你可以使用该标签告诉 JSDoc 该方法是异步方法。

## <span id="examples">示例</span>

下面的例子展示了一个使用 `@async` 标签的虚拟注释：

**虚拟注释使用 @async 标签**

```javascript
/**
 * Download data from the specified URL.
 *
 * @async
 * @function downloadData
 * @param {string} url - The URL to download from.
 * @return {Promise<string>} The data from the URL.
 */
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @async](http://usejsdoc.org/tags-async.html "tag @async")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>