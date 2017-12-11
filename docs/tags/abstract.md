# @abstract

## 内容列表 🕊️
* [同义词](#Synonyms "Synonyms")
* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="Synonyms">同义词</span>

`@virtual`

## <span id="overview">概述</span>

`@abstract` 标签用来标识必须被其他继承这些成员的对象实现或者重写的成员。

## <span id="examples">示例</span>

**子类实现父类的抽象方法**

```javascript
/**
 * Generic dairy product.
 * @constructor
 */
function DairyProduct() {}

/**
 * Check whether the dairy product is solid at room temperature.
 * @abstract
 * @return {boolean}
 */
DairyProduct.prototype.isSolid = function() {
    throw new Error('must be implemented by subclass!');
};

/**
 * Cool, refreshing milk.
 * @constructor
 * @augments DairyProduct
 */
function Milk() {}

/**
 * Check whether milk is solid at room temperature.
 * @return {boolean} Always returns false.
 */
Milk.prototype.isSolid = function() {
    return false;
};
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @abstract](http://usejsdoc.org/tags-abstract.html "tag abstract")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>