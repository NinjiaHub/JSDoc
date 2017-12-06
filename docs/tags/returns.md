# @returns

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="Synonyms">同义词</span>

`@returns`

## <span id="syntax">语法</span>

`@returns [{type}] [description]`

## <span id="overview">概述</span>

`@returns` 标签用来给方法的返回值添加文档注释。

## <span id="examples">示例</span>

如果要给 **generator** 函数添加文档注释，请使用 [@yields](https://ninjiahub.github.io/JSDoc/docs/tags/yields "tag @yields") 标签。

**标注返回值类型**

```javascript
/**
 * Returns the sum of a and b
 * @param {number} a
 * @param {number} b
 * @returns {number}
 */
function sum(a, b) {
    return a + b;
}
```

**标注返回值类型以及描述**

```javascript
/**
 * Returns the sum of a and b
 * @param {number} a
 * @param {number} b
 * @returns {number} Sum of a and b
 */
function sum(a, b) {
    return a + b;
}
```

**标注有多种类型的返回值**

```javascript
/**
 * Returns the sum of a and b
 * @param {number} a
 * @param {number} b
 * @param {boolean} retArr If set to true, the function will return an array
 * @returns {(number|Array)} Sum of a and b or an array that contains a, b and the sum of a and b.
 */
function sum(a, b, retArr) {
    if (retArr) {
        return [a, b, a + b];
    }
    return a + b;
}
```

**返回 promise**

```javascript
/**
 * Returns the sum of a and b
 * @param {number} a
 * @param {number} b
 * @returns {Promise} Promise object represents the sum of a and b
 */
function sumAsync(a, b) {
    return new Promise(function(resolve, reject) {
        resolve(a + b);
    });
}
```

## <span id="related">相关链接</span>

* [@param](https://ninjiahub.github.io/JSDoc/docs/tags/param "tag @param")
* [@yields](https://ninjiahub.github.io/JSDoc/docs/tags/yields "tag @yields")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - Using namepaths with JSDoc 3](http://usejsdoc.org/about-namepaths.html "namepaths")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>