# @global

## 内容列表 🕊️

* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="overview">概述</span>

`@global` 标签用来标明一个标识符在文档中应该被标记为全局标识符(即全局变量)。JSDoc 会忽略该标识符在源文件中的真实作用域。这个标签在标识局部定义、赋值给全局作用域的标识符时非常有用。

## <span id="examples">示例</span>

使用 @global 标签标识一个标识符的作用域为全局范围：

**将一个内部变量标记为全局变量**

```javascript
(function() {
    /** @global */
    var foo = 'hello foo';

    this.foo = foo;
}).apply(window);
```

## <span id="related">相关链接</span>

* [@inner](https://ninjiahub.github.io/JSDoc/docs/tags/inner "tag @inner")
* [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")
* [@memberof](https://ninjiahub.github.io/JSDoc/docs/tags/memberof "tag @memberof")
* [@static](https://ninjiahub.github.io/JSDoc/docs/tags/static "tag @static")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @global](http://usejsdoc.org/tags-global.html "tag @global")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>