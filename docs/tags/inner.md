# @inner

## 内容列表 🕊️

* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="overview">概述</span>

`@inner` 标签会将一个标识符标记为父标识符的内部成员，即该标识符可以通过 "Parent~Child" 的方式引用。

使用 `@inner` 标签将会覆盖文档变量中的默认作用域(除非该标识符在全局作用域中)。

## <span id="examples">示例</span>

**使用 @inner 标签将一个虚拟的文档变量标记为内部成员**

```javascript
/** @namespace MyNamespace */
/**
 * myFunction is now MyNamespace~myFunction.
 * @function myFunction
 * @memberof MyNamespace
 * @inner
 */
```

**注意：** 上面的例子我们可以使用 `@function MyNamespace~myFunction` 来代替 `@memberof` 和 `@inner` 标签。

**使用 @inner 标签**

```javascript
/** @namespace */
var MyNamespace = {
    /**
     * foo is now MyNamespace~foo rather than MyNamespace.foo.
     * @inner
     */
    foo: 1
};
```

上面的例子中，我们使用 `@inner` 标签将命名空间中的成员强制标记为内部成员(默认情况下 'foo' 是一个静态成员)，这意味着 **foo** 现在的 **长命名(longname)** 是 `MyNamespace~foo` 而不是 `MyNamespace.foo`。

## <span id="related">相关链接</span>

* [@global](https://ninjiahub.github.io/JSDoc/docs/tags/global "tag @global")
* [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")
* [@static](https://ninjiahub.github.io/JSDoc/docs/tags/static "tag @static")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @inner](http://usejsdoc.org/tags-inner.html "tag @inner")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>