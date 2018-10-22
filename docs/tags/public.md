# @public

## 内容列表 🕊️

* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="overview">概述</span>

`@public` 标签表示一个标识符应该被当作公开(public)来标记。

默认情况下，JSDoc 将所有标识符当成公开的来对待，所以该标签并不会影响生成的文档。然而，或许你更倾向于明确地使用 `@public` 标签，以便于其他人可以清楚地知道你想使该标识符公开。

在 JSDoc 3 中，`@public` 标签并不影响标识符的作用域。要改变标识符的作用域，请使用 [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")、[@static](https://ninjiahub.github.io/JSDoc/docs/tags/static "tag @static") 和 [@global](https://ninjiahub.github.io/JSDoc/docs/tags/global "tag @global") 标签。

## <span id="examples">示例</span>

**使用 @public 标签**

```javascript
/**
 * The Thingy class is available to all.
 * @public
 * @class
 */
function Thingy() {
    /**
     * The Thingy~foo member. Note that 'foo' is still an inner member
     * of 'Thingy', in spite of the @public tag.
     * @public
     */
    var foo = 0;
}
```

## <span id="related">相关链接</span>

* [@access](https://ninjiahub.github.io/JSDoc/docs/tags/access "tag @access")
* [@global](https://ninjiahub.github.io/JSDoc/docs/tags/global "tag @global")
* [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")
* [@package](https://ninjiahub.github.io/JSDoc/docs/tags/package "tag @package")
* [@private](https://ninjiahub.github.io/JSDoc/docs/tags/private "tag @private")
* [@protected](https://ninjiahub.github.io/JSDoc/docs/tags/protected "tag @protected")
* [@static](https://ninjiahub.github.io/JSDoc/docs/tags/static "tag @static")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @public](http://usejsdoc.org/tags-public.html "tag @public")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>