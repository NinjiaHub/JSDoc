# @fires

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="Synonyms">同义词</span>

`@emits`

## <span id="syntax">语法</span>

`@fires <className>#[event:]<eventName>`

## <span id="overview">概述</span>

`fires` 标签表示当前方法被调用时会触发一个特定类型的事件。使用 [@event](https://ninjiahub.github.io/JSDoc/docs/tags/event "tag @event") 标签给事件内容添加文档注释。

## <span id="examples">示例</span>

**触发 'drain' 事件的方法**

```javascript
/**
 * Drink the milkshake.
 *
 * @fires Milkshake#drain
 */
Milkshake.prototype.drink = function() {
    // ...
};
```

## <span id="related">相关链接</span>

* [@listens](https://ninjiahub.github.io/JSDoc/docs/tags/listens "tag @listens")
* [@event](https://ninjiahub.github.io/JSDoc/docs/tags/event "tag @event")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @fires](http://usejsdoc.org/tags-fires.html "tag @fires")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>