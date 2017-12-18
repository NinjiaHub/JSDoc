# @access

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@access <package|private|protected|public>`

## <span id="overview">概述</span>

`@access` 标签用来指定成员的访问等级。可以使用 `@access` 标签作为其他标签的同义词：

* `@access package` === `@package`，该选项在 JSDoc 3.5 及其之后的版本中可用
* `@access private` === `@private`
* `@access protected` === `@protected`
* `@access public` === `@public`

私有成员不会出现在生成的输出结果中，除非 JSDoc 在运行时使用了命令行选项 `-p/--private`。在 JSDoc 3.3.0 及其之后的版本中，可以通过使用 [命令行选项 -a/--access](https://ninjiahub.github.io/JSDoc/docs/start/about-commandline) 来修改这个默认行为。

注意，成员的访问等级与作用域是有区别的。比如，如果 `Parent` 有一个被标记为 `@public` 内部变量 `child`，`child` 变量仍被当作内部变量来对待，命名路由为 `Parent~child`。换言之，`child` 变量仍然拥有一个内部作用域，即使这个变量是公开的(public)。要改变文档变量的作用域，请使用 [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")、[@static](https://ninjiahub.github.io/JSDoc/docs/tags/static "tag @static") 和 [@global](https://ninjiahub.github.io/JSDoc/docs/tags/global "tag @global") 标签。

## <span id="examples">示例</span>

**使用 @access 标签作为其他标签的同义词**

```javascript
/** @constructor */
function Thingy() {

    /** @access private */
    var foo = 0;

    /** @access protected */
    this._bar = 1;

    /** @access package */
    this.baz = 2;

    /** @access public */
    this.pez = 3;

}

// same as...

/** @constructor */
function OtherThingy() {

    /** @private */
    var foo = 0;

    /** @protected */
    this._bar = 1;

    /** @package */
    this.baz = 2;

    /** @public */
    this.pez = 3;

}
```

## <span id="related">相关链接</span>

* [@global](https://ninjiahub.github.io/JSDoc/docs/tags/global "tag @global")
* [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")
* [@package](https://ninjiahub.github.io/JSDoc/docs/tags/package "tag @package")
* [@private](https://ninjiahub.github.io/JSDoc/docs/tags/private "tag @private")
* [@protected](https://ninjiahub.github.io/JSDoc/docs/tags/protected "tag @protected")
* [@public](https://ninjiahub.github.io/JSDoc/docs/tags/public "tag @public")
* [@static](https://ninjiahub.github.io/JSDoc/docs/tags/static "tag @static")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @access](http://usejsdoc.org/tags-access.html "tag @access")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>