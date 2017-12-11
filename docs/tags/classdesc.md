# @classdesc

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@classdesc <some description>`

## <span id="overview">概述</span>

`@classdesc` 标签用来给类添加描述，应该与构造函数的描述分开。`@classdesc` 标签应该与 [@class](https://ninjiahub.github.io/JSDoc/docs/tags/class "tag @class")(或者 @constructor) 一起使用。

在 JSDoc 3 中，`@classdesc` 标签与之前版本中 `@class` 标签的功能重复了。在 3.x 版本中，`@class` 标签的语法、功能与 `@constructor` 标签一致，`@classdesc` 标签能更准确地表达它的意图：将类的描述添加到文档注释中。

## <span id="examples">示例</span>

如下所示：下面的类有两个描述，一个适用于当前函数，另外一个适用于一般类。

**同时包含构造器函数描述和类描述的文档变量(doclet)**

```javascript
/**
 * This is a description of the MyClass constructor function.
 * @class
 * @classdesc This is a description of the MyClass class.
 */
function MyClass() {
}
```
## <span id="related">相关链接</span>

* [@class](https://ninjiahub.github.io/JSDoc/docs/tags/class "tag @class")
* [@description](https://ninjiahub.github.io/JSDoc/docs/tags/description "tag @description")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @class](http://usejsdoc.org/tags-classdesc.html "tag @class")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>