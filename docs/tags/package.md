# @package

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

JSDoc 标签字典(默认开启)：

`@package`

[Closure Compiler](https://github.com/google/closure-compiler/wiki/Annotating-JavaScript-for-the-Closure-Compiler#jsdoc-tags) 标签字典：

`@package [{typeExpression}]`

## <span id="overview">概述</span>

`@package` 标签会将一个标识符标记为包私有的。通常，该标签表示一个标识符仅在与当前文件处于同级目录的文件的代码中可用。该标签在 JSDoc 3.5.0 及其之后的版本中可用。

默认情况下，被 `@pakcage` 标签标记的标识符仍然会出现在文档中。在 JSDoc 3.3.0 及其之后的版本中，可以通过使用 [命令行选项 -a/--access](https://ninjiahub.github.io/JSDoc/docs/start/about-commandline) 来修改这个默认行为。

`@package` 标签与 `@access package` 是等价的。

## <span id="examples">示例</span>

## <span id="related">相关链接</span>

* [@access](https://ninjiahub.github.io/JSDoc/docs/tags/access "tag @access")
* [@global](https://ninjiahub.github.io/JSDoc/docs/tags/global "tag @global")
* [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")
* [@private](https://ninjiahub.github.io/JSDoc/docs/tags/private "tag @private")
* [@protected](https://ninjiahub.github.io/JSDoc/docs/tags/protected "tag @protected")
* [@public](https://ninjiahub.github.io/JSDoc/docs/tags/public "tag @public")
* [@static](https://ninjiahub.github.io/JSDoc/docs/tags/static "tag @static")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @package](http://usejsdoc.org/tags-package.html "tag @package")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>