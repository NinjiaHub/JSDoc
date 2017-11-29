# @class

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [语法](#Syntax "Syntax")
* [概述](#Overview "Overview")
* [示例](#Examples "Examples")
* [相关链接](#related "related")

## <span id="Synonyms">同义词</span>

`@construcor`

## <span id="Syntax">语法 </span>

`@class [<type> <name>]`

## <span id="Overview">概述</span>

**@class** 标签用来标记作为构造器调用的函数，即该函数被 **new** 关键字进行构造调用并返回一个实例。

## <span id="Examples">示例</span>

**一个用来构造 Person 实例的函数**

```javascript
/**
 * Creates a new Person.
 * @class
 */
function Person() {
}

var p = new Person();
```
## <span id="related">相关链接</span>

* [@constructs](https://ninjiahub.github.io/JSDoc/docs/tags/constructs "tag @ constructs")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @class](http://usejsdoc.org/tags-class.html "tag class")。

如有版权问题请联系译者。

侵删。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>