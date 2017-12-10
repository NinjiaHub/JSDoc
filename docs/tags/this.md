# @this

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@this <namePath>`

## <span id="overview">概述</span>

当在另外一个标识符中使用时，`@this` 标签用来表示 **this** 指向哪个对象。

## <span id="examples">示例</span>

下面的例子中，`@tag` 标签会使 `this.name` 被标记为 `Greeter#name`，而不是被标记为一个全局的标识符 `name`。

```javascript
/** @constructor */
function Greeter(name) {
    setName.apply(this, name);
}

/** @this Greeter */
function setName(name) {
    /** document me */
    this.name = name;
}
```

## <span id="related">相关链接</span>

* [@memberof](https://ninjiahub.github.io/JSDoc/docs/tags/memberof "tag @memberof")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @this](http://usejsdoc.org/tags-this.html "tag @this")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>