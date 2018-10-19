# @override

## 内容列表 🕊️

* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="overview">概述</span>

`@override` 标签标示一个标识符重写了父类中的同名标识符。

提供该标签是为了与 [Closure Compiler](https://developers.google.com/closure/compiler/) 兼容。默认情况下，JSDoc 会自动标识重写父类中同名标识符的标识符。

如果你的 JSDoc 注释中包含了 [@inheritdoc](https://ninjiahub.github.io/JSDoc/docs/tags/inheritdoc "tag @inheritdoc") 标签，则不需要再次包含 @override 标签。@inheritdoc 标签的出现包含 @override 标签也存在的意思。

## <span id="examples">示例</span>

下面的例子展示了如何标示一个标识符重写了父类中的同名属性：

**重写父类中的方法**

```javascript
/**
 * @classdesc Abstract class representing a network connection.
 * @class
 */
function Connection() {}

/**
 * Open the connection.
 */
Connection.prototype.open = function() {
    // ...
};


/**
 * @classdesc Class representing a socket connection.
 * @class
 * @augments Connection
 */
function Socket() {}

/**
 * Open the socket.
 * @override
 */
Socket.prototype.open = function() {
    // ...
};
```

## <span id="related">相关链接</span>

* [@inheritdoc](https://ninjiahub.github.io/JSDoc/docs/tags/inheritdoc "tag @inheritdoc")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @override](http://usejsdoc.org/tags-override.html "tag @override")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>