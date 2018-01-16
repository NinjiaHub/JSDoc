# @exports

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@exports <moduleName>`

在 JSDoc 3.3.0 及其之后的版本中，`<moduleName>` 可能会包含 `module:` 前缀。而在之前的版本中，一定要删除该前缀，因为之前的版本不认识该前缀，会导致其他文档注释无法正确引用模块。

## <span id="overview">概述</span>

当给 JavaScript 模块添加文档注释时，如果该模块导出的并不是 “exports” 对象或者 “module.exports” 属性，则需要使用 @exports 标签来标记该模块。

## <span id="examples">示例</span>

在使用 “exports” 对象的模块中，不需要使用 @exports 标签。JSDoc 会自动识别该对象(exports) 的成员要被导出。同样，JSDoc 也能自动识别出 Node.js 模块中的特殊属性 “module.exports”。

**CommonJS 模块**

```javascript
/**
 * A module that says hello!
 * @module hello/world
 */

/** Say hello. */
exports.sayHello = function() {
    return 'Hello world';
};
```

**Node.js 模块**

```javascript
/**
 * A module that shouts hello!
 * @module hello/world
 */

/** SAY HELLO. */
module.exports = function() {
    return "HELLO WORLD";
};
```

**导出对象字面量的 AMD 模块**

```javascript
define(function() {

    /**
     * A module that whispers hello!
     * @module hello/world
     */
    var exports = {};

    /** say hello. */
    exports.sayHello = function() {
        return 'hello world';
    };

    return exports;
});
```

**导出构造器的 AMD 模块**

```javascript
define(function() {
    /**
     * A module that creates greeters.
     * @module greeter
     */

    /**
     * @constructor
     * @param {string} subject - The subject to greet.
     */
    var exports = function(subject) {
        this.subject = subject || 'world';
    };

    /** Say hello to the subject. */
    exports.prototype.sayHello = function() {
        return 'Hello ' + this.subject;
    };

    return exports;
});
```

如果模块的导出对象名字不是 “exports” 或者 “module.exports”，使用 @exports 标签来标识导出对象。

**导出对象的 AMD 模块**

```javascript
define(function () {

    /**
     * A module that says hello!
     * @exports hello/world
     */
    var ns = {};

    /** Say hello. */
    ns.sayHello = function() {
        return 'Hello world';
    };

    return ns;
});
```

## <span id="related">相关链接</span>

* [@module](https://ninjiahub.github.io/JSDoc/docs/tags/module "tag @module")
* [CommonJS Module](https://ninjiahub.github.io/JSDoc/docs/examples/commonjs-modules "examples commonjs-modules")
* [AMD Module](https://ninjiahub.github.io/JSDoc/docs/examples/amd-modules "examples amd-modules")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @exports](http://usejsdoc.org/about-exports.html "tag @exports")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>