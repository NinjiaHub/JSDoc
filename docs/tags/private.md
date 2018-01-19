# @private

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

JSDoc 标签字典(默认开启)：

`@private`

[Closure Compiler](https://github.com/google/closure-compiler/wiki/Annotating-JavaScript-for-the-Closure-Compiler#jsdoc-tags) 标签字典：

`@private [{typeExpression}]`

## <span id="overview">概述</span>

`@private` 标签将标识符标记为私有成员。私有成员不会出现在生成的输出结果中，除非 JSDoc 在运行时使用了命令行选项 `-p/--private`。在 JSDoc 3.3.0 及其之后的版本中，可以通过使用 [命令行选项 -a/--access](https://ninjiahub.github.io/JSDoc/docs/start/about-commandline) 来修改这个默认行为。

`@private` 标签不会被子成员继承。比如，如果 `@private` 标签被添加到一个命名空间上，该命名空间的子成员仍然会出现在生成的输出中；因为该命名空间是私有的，所以成员的命名路由中不会出现该命名空间。

`@private` 标签与 `@access private` 是等价的。

## <span id="examples">示例</span>

下面的例子中，`Documents` 和 `Documents.Newspaper` 会出现在生成的文档中，但是 `Documents.Diary` 不会出现在生成的文档中。

**使用 @private 标签**

```javascript
/** @namespace */
var Documents = {
    /**
     * An ordinary newspaper.
     */
    Newspaper: 1,
    /**
     * My diary.
     * @private
     */
    Diary: 2
};
```

## <span id="related">相关链接</span>

* [@access](https://ninjiahub.github.io/JSDoc/docs/tags/access "tag @access")
* [@global](https://ninjiahub.github.io/JSDoc/docs/tags/global "tag @global")
* [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")
* [@package](https://ninjiahub.github.io/JSDoc/docs/tags/package "tag @package")
* [@protected](https://ninjiahub.github.io/JSDoc/docs/tags/protected "tag @protected")
* [@public](https://ninjiahub.github.io/JSDoc/docs/tags/public "tag @public")
* [@static](https://ninjiahub.github.io/JSDoc/docs/tags/static "tag @static")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @private](http://usejsdoc.org/tags-private.html "tag @private")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>