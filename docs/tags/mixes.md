# @mixes

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@mixes <OtherObjectPath>`

## <span id="overview">概述</span>

@mixes 标签表示当前对象要将 **OtherObjectPath** 中的所有成员混入到当前对象。被混入的对象 **OtherObjectPath** 是一个 [@mixin](https://ninjiahub.github.io/JSDoc/docs/tags/mixin "tag @mixin")。

## <span id="examples">示例</span>

首先，我们使用 [@mixin](https://ninjiahub.github.io/JSDoc/docs/tags/mixin "tag @mixin") 标签来标记一个 **mixin**：

**@mixin**

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

接下来，我们添加一个 **FormButton** 类，然后调用 `mixin` 方法将所有事件相关的方法混入到 **FormButton** 中，以便于 **FormButton** 也可以触发事件以及具有监听器。我们使用 @mixes 标签表示 FormButton 混入所有事件相关的函数。

**使用 @mixes 标签**

```javascript
/**
 * @constructor FormButton
 * @mixes Eventful
 */
var FormButton = function() {
    // code...
};
FormButton.prototype.press = function() {
  this.fire('press', {});
}
mix(Eventful).into(FormButton.prototype);
```

## <span id="related">相关链接</span>

* [@borrows](https://ninjiahub.github.io/JSDoc/docs/tags/borrows "tag @borrows")
* [@class](https://ninjiahub.github.io/JSDoc/docs/tags/class "tag @class")
* [@mixin](https://ninjiahub.github.io/JSDoc/docs/tags/mixin "tag @mixin")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @mixes](http://usejsdoc.org/tags-mixes.html "tag @mixes")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>