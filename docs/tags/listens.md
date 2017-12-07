# @listens

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@listens <eventName>`

## <span id="overview">概述</span>

`@listens` 标签表示一个标识符监听一个特定的事件。使用 [@event](https://ninjiahub.github.io/JSDoc/docs/tags/event "tag @event") 标签给事件的内容添加文档注释。

## <span id="examples">示例</span>

下面的例子展示了如何给一个事件 `module:hurler~event:snowball` 以及用来监听事件的方法 `module:playground/monitor.reportThrowage` 添加文档注释。

**给事件及其监听器添加文档注释**

```javascript
define('hurler', [], function () {
    /**
     * Event reporting that a snowball has been hurled.
     *
     * @event module:hurler~snowball
     * @property {number} velocity - The snowball's velocity, in meters per second.
     */

    /**
     * Snowball-hurling module.
     *
     * @module hurler
     */
    var exports = {
        /**
         * Attack an innocent (or guilty) person with a snowball.
         *
         * @method
         * @fires module:hurler~snowball
         */
        attack: function () {
            this.emit('snowball', { velocity: 10 });
        }
    };

    return exports;
});

define('playground/monitor', [], function () {
    /**
     * Keeps an eye out for snowball-throwers.
     *
     * @module playground/monitor
     */
    var exports = {
        /**
         * Report the throwing of a snowball.
         *
         * @method
         * @param {module:hurler~event:snowball} e - A snowball event.
         * @listens module:hurler~event:snowball
         */
        reportThrowage: function (e) {
            this.log('snowball thrown: velocity ' + e.velocity);
        }
    };

    return exports;
});
```

## <span id="related">相关链接</span>

* [@event](https://ninjiahub.github.io/JSDoc/docs/tags/event "tag @event")
* [@fires](https://ninjiahub.github.io/JSDoc/docs/tags/fires "tag @fires")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @listens](http://usejsdoc.org/tags-listens.html "tag @listens")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>