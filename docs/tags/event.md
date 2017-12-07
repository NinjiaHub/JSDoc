# @event

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@event <className>#[event:]<eventName>`

## <span id="overview">概述</span>

`@event` 标签用来给事件添加文档注释。一个典型事件的表示方法为一个有一系列定义属性的对象。

在使用 `@event` 标签标注事件之后，可以使用 `@fires` 标签标示一个可以触发该事件的方法，并且可以使用 `@listens` 标签标示一个监听该事件的标识符。

JSDoc 会自动在每一个事件名字前加上命名空间 `event:`。通常，如果要在其他文档中链接该事件时，必须要使用命名空间。(@fires 事件是一个值得注意的例外，该标签允许省略命名空间。)

**注意：** JSDoc 3 使用 @event 标签给事件内容添加文档注释。JSDoc Toolkit 2 使用 @event 标示一个当出现同名事件时可以调用的方法。

## <span id="examples">示例</span>

下面的例子展示了如何给 **Hurl** 类中的 **snowball** 事件添加文档注释。该事件包含了一个只有一个属性的对象。

**将方法调用标记为事件**

```javascript
/**
 * Throw a snowball.
 *
 * @fires Hurl#snowball
 */
Hurl.prototype.snowball = function() {
    /**
     * Snowball event.
     *
     * @event Hurl#snowball
     * @type {object}
     * @property {boolean} isPacked - Indicates whether the snowball is tightly packed.
     */
    this.emit('snowball', {
        isPacked: this._snowball.isPacked
    });
};
```

**使用命名 doclet 给事件添加文档注释**

```javascript
/**
 * Throw a snowball.
 *
 * @fires Hurl#snowball
 */
Hurl.prototype.snowball = function() {
    // ...
};

/**
 * Snowball event.
 *
 * @event Hurl#snowball
 * @type {object}
 * @property {boolean} isPacked - Indicates whether the snowball is tightly packed.
 */
```

## <span id="related">相关链接</span>

* [@listens](https://ninjiahub.github.io/JSDoc/docs/tags/listens "tag @listens")
* [@fires](https://ninjiahub.github.io/JSDoc/docs/tags/fires "tag @fires")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @event](http://usejsdoc.org/tags-event.html "tag @event")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>