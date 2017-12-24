# @static

## 内容列表 🕊️

* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="overview">概述</span>

`@static` 标签表示一个标识符可以直接通过父标识符引用而无需在实例化后的实例上调用。

使用 `@static` 标签将会覆盖文档变量中的默认作用域(除非该标识符在全局作用域中)。

## <span id="examples">示例</span>

下面的例子与使用 `@function MyNamespace.myFunction` 并省略 @memberof 与 @static 标签有同样的效果：

**在虚拟注释(不作用于具体代码)中使用 @static 标签**

```javascript
/** @namespace MyNamespace */

/**
 * @function myFunction
 * @memberof MyNamespace
 * @static
 */
```

下面的例子强制模块中的内部成员被标记为静态成员：

**使用 @static 标签覆盖默认作用域**

```javascript
/** @module Rollerskate */

/**
 * The 'wheel' variable is documented as Rollerskate.wheel
 * rather than Rollerskate~wheel.
 * @static
 */
var wheel = 1;

```

## <span id="related">相关链接</span>

* [@global](https://ninjiahub.github.io/JSDoc/docs/tags/global "tag @global")
* [@inner](https://ninjiahub.github.io/JSDoc/docs/tags/inner "tag @inner")
* [@instance](https://ninjiahub.github.io/JSDoc/docs/tags/instance "tag @instance")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @static](http://usejsdoc.org/tags-static.html "tag @static")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>