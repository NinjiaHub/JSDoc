# @kind

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@kind <kindName>`

`<kindname>`列表：

* class
* constant
* event
* external
* file
* function
* member
* mixin
* module
* namespace
* typedef

## <span id="overview">概述</span>

`@kind` 标签用来标明正在给哪种标识(比如：一个**类**或者一个**模块**)添加文档注释。一个标识的 **kind** 与 **type** 是有区别的。

**译注：type 标签主要用来标识一个标识符在 JavaScript 中的原生类型(包括引用类型和基本数据类型)**

通常情况下并不需要手动使用 `@kind` 标签，因为标识符的种类(kind) 一般通过其他标签来体现。例如，使用 `@class` 标签意味着 `@kind class`，使用 `@namespace` 与 `@kind namespace` 表示同样的意义。

## <span id="examples">示例</span>

**使用 @kind 标签**

```javascript
// The following examples produce the same result:

/**
 * A constant.
 * @kind constant
 */
const asdf = 1;

/**
 * A constant.
 * @constant
 */
const asdf = 1;
```

当标签和 **@kind** 冲突时(例如，同时使用 **@module** 将种类设置为 **module** 并且使用 **@kind** 将种类设置为 **constant**)，种类由最后的声明决定。

**@kind 声明冲突**

```javascript
/**
 * This will show up as a constant
 * @module myModule
 * @kind constant
 */

/**
 * This will show up as a module.
 * @kind constant
 * @module myModule
 */
```

## <span id="related">相关链接</span>

* [@type](https://ninjiahub.github.io/JSDoc/docs/tags/type "tag @type")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - Using namepaths with JSDoc 3](http://usejsdoc.org/about-namepaths.html "namepaths")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>