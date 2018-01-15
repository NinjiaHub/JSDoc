# @example

## 内容列表 🕊️

* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="overview">概述</span>

提供一个例子来演示如何使用被标记项。该标签后的文字将会以高亮代码的形式展示。

## <span id="examples">示例</span>

注意，一个文档变量可以有多个示例。

**标注示例**

```javascript
/**
 * Solves equations of the form a * x = b
 * @example
 * // returns 2
 * globalNS.method1(5, 10);
 * @example
 * // returns 3
 * globalNS.method(5, 15);
 * @returns {Number} Returns the value of x for the equation.
 */
globalNS.method1 = function (a, b) {
    return b / a;
};
```

可以通过在 `@example` 标签后添加 `<caption></caption>` 的方式给示例添加标题。

**有标题的标注示例**

```javascript
/**
 * Solves equations of the form a * x = b
 * @example <caption>Example usage of method1.</caption>
 * // returns 2
 * globalNS.method1(5, 10);
 * @returns {Number} Returns the value of x for the equation.
 */
globalNS.method1 = function (a, b) {
    return b / a;
};
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @example](http://usejsdoc.org/tags-example.html "tag @example")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>