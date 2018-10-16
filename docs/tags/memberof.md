# @memberof

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

* `@memberof <parentNamepath>`
* `@memberof! <parentNamepath>`

## <span id="overview">概述</span>

`@memberof` 标签用来标示一个成员标识符属于一个父标识符。

默认情况下，@memberof 标签将成员标识符标记为静态成员。对于内部成员以及实例成员，可以在命名路由后使用范围符号，或者使用 [@inner](https://ninjiahub.github.io/JSDoc/docs/tags/inner "tag @inner") 标签和 [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")。

@memberof 标签的“强制”版本 **@memberof!**，强制标记一个对象属于一个特定的父标识符 A，即使这个对象有一个明显不是 A 的父标识符 B。

## <span id="examples">示例</span>

下面的例子中，函数 `hammer` 通常会被标记为全局函数，这是因为这个函数实际上是一个全局函数，但该函数也是命名空间 `Tools` 的成员，这也就是为什么我们要给该函数添加文档注释。解决办法就是添加一个 `@memberof` 标签：

```javascript
/** @namespace */
var Tools = {};

/** @memberof Tools */
var hammer = function() {
};

Tools.hammer = hammer;
```

对于类的实例方法，可以使用语法 `@memberof ClassName.prototype` 或者 `@memberof ClassName#` 。或者，也可以将 `@memberof ClassName` 和 `@instance` 标签结合起来使用。

**@memberof 和 类原型一起使用**

```javascript
/** @class Observable */
create(
    'Observable',
    {
        /**
         * This will be a static member, Observable.cache.
         * @memberof Observable
         */
        cache: [],

        /**
         * This will be an instance member, Observable#publish.
         * @memberof Observable.prototype
         */
        publish: function(msg) {},

        /**
         * This will also be an instance member, Observable#save.
         * @memberof Observable#
         */
        save: function() {},

        /**
         * This will also be an instance member, Observable#end.
         * @memberof Observable
         * @instance
         */
        end: function() {}
    }
);
```

下面的例子使用了 `@memberof` 标签的“强制”版本 `@memberof!` 来标记一个类(Data)的实例成员对象(Data#point)的属性。

当使用 `@property` 标签给一个属性添加文档注释时，不能通过使用 **长名称(longname，namepaths)** 链接到该属性。可以通过使用 `@alias` 标签和 `@memberof!` 标签告诉 JSDoc **Data#point.y** 应该被标记为 **Data#** 的成员 **point.y**，而不是被标记为 **Data#** 的成员 **point** 的成员 **y**。

**使用 @memberof!**

```javascript
/** @class */
function Data() {
    /**
     * @type {object}
     * @property {number} y This will show up as a property of `Data#point`,
     * but you cannot link to the property as {@link Data#point.y}.
     */
    this.point = {
        /**
         * The @alias and @memberof! tags force JSDoc to document the
         * property as `point.x` (rather than `x`) and to be a member of
         * `Data#`. You can link to the property as {@link Data#point.x}.
         * @alias point.x
         * @memberof! Data#
         */
        x: 0,
        y: 1
    };
}
```

## <span id="related">相关链接</span>

* [@name](https://ninjiahub.github.io/JSDoc/docs/tags/name "tag @name")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @memberof](http://usejsdoc.org/tags-memberof.html "tag @memberof")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>