# @mixin

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@mixin [<MixinName>]`

## <span id="overview">概述</span>

一个 Mixin 提供了想要添加到其他对象中的功能。可以直接使用 @mixin 标签表示一个对象是一个 **mixin**，然后可以在想要使用该 mixin 的对象上添加 **@mixes** 标签。

## <span id="examples">示例</span>

**使用 @mixin 标签**

```javascript
/**
 * This provides methods used for event handling. It's not meant to
 * be used directly.
 *
 * @mixin
 */
var Eventful = {
    /**
     * Register a handler function to be called whenever this event is fired.
     * @param {string} eventName - Name of the event.
     * @param {function(Object)} handler - The handler to call.
     */
    on: function(eventName, handler) {
        // code...
    },

    /**
     * Fire an event, causing all handlers for that event name to run.
     * @param {string} eventName - Name of the event.
     * @param {Object} eventData - The data provided to each handler.
     */
    fire: function(eventName, eventData) {
        // code...
    }
};

```

## <span id="related">相关链接</span>

* [@borrows](https://ninjiahub.github.io/JSDoc/docs/tags/borrows "tag @borrows")
* [@class](https://ninjiahub.github.io/JSDoc/docs/tags/class "tag @class")
* [@mixes](https://ninjiahub.github.io/JSDoc/docs/tags/mixes "tag @mixes")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @mixin](http://usejsdoc.org/tags-mixin.html "tag @mixin")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>