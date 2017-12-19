# @interface

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

JSDoc 标签字典(默认开启)：

`@protected `

[Closure Compiler](https://github.com/google/closure-compiler/wiki/Annotating-JavaScript-for-the-Closure-Compiler#jsdoc-tags) 标签字典：

`@protected [{typeExpression}]`

## <span id="overview">概述</span>

`@interface` 标签将一个标识符标记为可以被其他标识符实现的接口。例如，你在代码里定义了一个方法和属性都不完整的父类，在这种情况下你可以给该父类添加 `@interface` 标签，标示继承该父类的子类必须实现该父类的方法和属性。

将 `@interface` 标签添加到标示接口的顶层(top-level)标识符上(比如 构造函数)，不需要将 `@interface` 标签添加到接口的每一个成员上。

如果你在使用 JSDoc 标签字典(默认开启)，也可以通过虚拟注释来定义接口，而不需要写代码来声明接口。详情请查看 [虚拟注释定义接口](#virtual-comment)。

## <span id="examples">示例</span>

下面的例子中，`Color` 函数标示一个可以被其他类继承并实现的接口：

**使用 @interface 标签**

```javascript
/**
 * Interface for classes that represent a color.
 *
 * @interface
 */
function Color() {}

/**
 * Get the color as an array of red, green, and blue values, represented as
 * decimal numbers between 0 and 1.
 *
 * @returns {Array<number>} An array containing the red, green, and blue values,
 * in that order.
 */
Color.prototype.rgb = function() {
    throw new Error('not implemented');
};
```

下面的例子使用虚拟注释代替代码来定义接口：

**<span id="virtual-comment">虚拟注释定义接口</span>**

```javascript
/**
 * Interface for classes that represent a color.
 *
 * @interface Color
 */

/**
 * Get the color as an array of red, green, and blue values, represented as
 * decimal numbers between 0 and 1.
 *
 * @function
 * @name Color#rgb
 * @returns {Array<number>} An array containing the red, green, and blue values,
 * in that order.
 */
```

## <span id="related">相关链接</span>

* [@implements](https://ninjiahub.github.io/JSDoc/docs/tags/implements "tag @implements")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @interface](http://usejsdoc.org/tags-interface.html "tag @interface")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>