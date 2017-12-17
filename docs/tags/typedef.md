# @typedef

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@typedef [<type>] <namepath>`

## <span id="overview">概述</span>

`@typedef` 标签在标记自定义的类型时非常好用，尤其是希望重复多次引用该类型时。这些自定义的类型可以在其他希望使用类型的标签中使用，比如 [@param](https://ninjiahub.github.io/JSDoc/docs/tags/param "tag @param") 标签和 [@type](https://ninjiahub.github.io/JSDoc/docs/tags/type "tag @type") 标签。

使用 [@callback](https://ninjiahub.github.io/JSDoc/docs/tags/callback "tag @callback") 标签标记回调函数的类型。

## <span id="examples">示例</span>

下面的例子定义了一个可以包含数字或者表示数字的字符串的复合类型：

**使用 @typedef 标签**

```javascript
/**
 * A number, or a string containing a number.
 * @typedef {(number|string)} NumberLike
 */

/**
 * Set the magic number.
 * @param {NumberLike} x - The magic number.
 */
function setMagicNumber(x) {
}
```

下面的例子定义了一个更为复杂的类型，即一个对象包含若干个属性，并且给该类型设置了命名路由，以便与使用该类型的类一起展示。因为类型定义实际上并没有被类所暴露出来，所以通常将类型定义标记为内部成员。

**使用 @typedef 定义一个复杂类型**

```javascript
/**
 * The complete Triforce, or one or more components of the Triforce.
 * @typedef {Object} WishGranter~Triforce
 * @property {boolean} hasCourage - Indicates whether the Courage component is present.
 * @property {boolean} hasPower - Indicates whether the Power component is present.
 * @property {boolean} hasWisdom - Indicates whether the Wisdom component is present.
 */

/**
 * A class for granting wishes, powered by the Triforce.
 * @class
 * @param {...WishGranter~Triforce} triforce - One to three {@link WishGranter~Triforce} objects
 * containing all three components of the Triforce.
 */
function WishGranter(triforce) {}
```

## <span id="related">相关链接</span>

* [@callback](https://ninjiahub.github.io/JSDoc/docs/tags/callback "tag @callback")
* [@param](https://ninjiahub.github.io/JSDoc/docs/tags/param "tag @param")
* [@type](https://ninjiahub.github.io/JSDoc/docs/tags/type "tag @type")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @typedef](http://usejsdoc.org/tags-typedef.html "tag @typedef")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>