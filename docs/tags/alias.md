# @alias

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@alias <aliasNamepath>`

## <span id="overview">概述</span>

@alias 使 JSDoc 对一个成员的所有引用都像该成员有一个别名一样。该标签在一个内部方法中定义类时非常有用，在这种情况下，你可以使用 @alias 标签告诉 JSDoc 要如何在应用中暴露该类。

虽然 @alias 标签与 @name 标签听起来很像，但是它们的表现有很大的区别。@name 标签会使 JSDoc 忽略任何与注释有关联的代码。例如，当 JSDoc 处理下面的代码时，它会忽略 `bar` 的注释是关联到一个函数的：

```javascript
/**
 * Bar function.
 * @name bar
 */
function foo() {}
```

@alias 标签会使 JSDoc 假装成员 A 的真正的名字是 成员 B。例如，当 JSDoc 处理下面的代码时，它识别出 `foo` 是一个函数，然后在文档中将 `foo` 重命名为 `bar`：

```javascript
/**
 * Bar function.
 * @alias bar
 */
function foo() {}
```

## <span id="examples">示例</span>

假设你正在使用一个类框架，当你使用该框架定义类时，框架要求输入一个“构造函数”，此时可以使用 @alias 标签告诉 JSDoc 如何在 app 中暴露该类。

下面的例子中，@alias 标签告诉 JSDoc 将匿名函数作为类 “trackr.CookieManager” 的构造器。在函数中，JSDoc 将关键字 `this` 解析为 trackr.CookieManager，所以 “value” 的命名路由为 “trackr.CookieManager#value”。

**匿名构造器函数使用 @alias 标签**

```javascript
Klass('trackr.CookieManager',

    /**
     * @class
     * @alias trackr.CookieManager
     * @param {Object} kv
     */
    function(kv) {
        /** The value. */
        this.value = kv;
    }

);
```

@alias 标签也可以用在 IIFE(立即执行函数) 创建的成员上。@alias 标签告诉 JSDoc 这些创建的成员会暴露在 IIFE 的作用域外。

**对命名空间的静态成员使用 @alias 标签**

```javascript
/** @namespace */
var Apple = {};

(function(ns) {
    /**
     * @namespace
     * @alias Apple.Core
     */
    var core = {};

    /** Documented as Apple.Core.seed */
    core.seed = function() {};

    ns.Core = core;
})(Apple);
```

对于定义在对象字面量中的成员，也可以使用 @alias 标签来代替 [@lends](https://ninjiahub.github.io/JSDoc/docs/tags/lends "tag @lends") 标签：

**对象字面量使用 @alias 标签**

```javascript
// Documenting objectA with @alias

var objectA = (function() {

    /**
     * Documented as objectA
     * @alias objectA
     * @namespace
     */
    var x = {
        /**
         * Documented as objectA.myProperty
         * @member
         */
        myProperty: 'foo'
    };

    return x;
})();

// Documenting objectB with @lends

/**
 * Documented as objectB
 * @namespace
 */
var objectB = (function() {

    /** @lends objectB */
    var x = {
        /**
         * Documented as objectB.myProperty
         * @member
         */
        myProperty: 'bar'
    };

    return x;
})();
```

## <span id="related">相关链接</span>

* [@lends](https://ninjiahub.github.io/JSDoc/docs/tags/lends "tag @lends")
* [@name](https://ninjiahub.github.io/JSDoc/docs/tags/name "tag @name")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @alias](http://usejsdoc.org/tags-alias.html "tag @alias")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>