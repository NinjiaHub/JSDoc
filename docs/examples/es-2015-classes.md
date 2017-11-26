# ES 2015 Classes

## 内容列表 🕊️

* [简单类](#simple "documenting a simple class")
* [继承类](#extends "extending classes")
* [相关链接](#related "related links")

通过 **JSDoc 3** 给遵循 [ECMAScript 2015 规范](http://www.ecma-international.org/ecma-262/6.0/#sec-class-definitions) 的类写注释是一件很容易的事情。在 **ES 2015 中的class** 不需要使用`@class`以及`@extends`这类标签 - **JSDoc** 会通过解析代码自动识别类以及类的构造器。**JSDoc 3.4.0** 及其之后的版本开始支持 **ES 2015 中的class**。

## <span id="simple">给简单类添加注释</span>

下面的例子展示了如何给一个具有构造器、两个实例方法以及一个静态方法的类添加注释：

**简单 ES 2015 类**

```javascript
/** Class representing a point. */
class Point {
    /**
     * Create a point.
     * @param {number} x - The x value.
     * @param {number} y - The y value.
     */
    constructor(x, y) {
        // ...
    }

    /**
     * Get the x value.
     * @return {number} The x value.
     */
    getX() {
        // ...
    }

    /**
     * Get the y value.
     * @return {number} The y value.
     */
    getY() {
        // ...
    }

    /**
     * Convert a string containing two comma-separated numbers into a point.
     * @param {string} str - The string containing two comma-separated numbers.
     * @return {Point} A Point object.
     */
    static fromString(str) {
        // ...
    }
}
```

也可以给一个初始化变量或者常量、以类表达式的形式定义的类添加注释。

**ES 2015 类表达式**

```javascript
/** Class representing a point. */
const Point = class {
    // and so on
}
```

## <span id="extends">继承类注释</span>

当使用`extends`关键字来继承一个已经存在的类时，需要告诉 JSDoc 要继承的类是哪个。可以通过 [@augments](https://ninjiahub.github.io/JSDoc/docs/tags/augments) 或者 [@extends](https://ninjiahub.github.io/JSDoc/docs/tags/extends) 标签来实现。

例如，继承上面的`Point`类：

**继承一个 ES 2015 中的类**

```javascript
/**
 * Class representing a dot.
 * @extends Point
 */
class Dot extends Point {
    /**
     * Create a dot.
     * @param {number} x - The x value.
     * @param {number} y - The y value.
     * @param {number} width - The width of the dot, in pixels.
     */
    constructor(x, y, width) {
        // ...
    }

    /**
     * Get the dot's width.
     * @return {number} The dot's width, in pixels.
     */
    getWidth() {
        // ...
    }
}
```

## <span id="related">相关链接</span> 🕸

* [@augments](https://ninjiahub.github.io/JSDoc/docs/tags/augments)

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - ES 2015 Classes](http://usejsdoc.org/howto-es2015-classes.html)。

如有版权问题请联系译者。

侵删。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>