# @member

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="Synonyms">同义词</span>

`@var`

## <span id="syntax">语法</span>

`@member [<type>] [<name>]`

## <span id="overview">概述</span>

`@member` 标签用来标记一个没有更详细种类(例如 **class**、**function**、**constant** 等)的成员。一个成员可以设置 **类型** 以及 **名字**。

## <span id="examples">示例</span>

**Data#point 使用 @member 标示**

```javascript
/** @class */
function Data() {
    /** @member {Object} */
    this.point = {};
}
```

下面是一个使用 `@member` 标签的同义词 `@var` 来给(虚拟) 变量 'foo' 添加文档注释的例子：

**使用 @var 标签给虚拟成员添加文档注释**

```javascript
/**
 * A variable in the global namespace called 'foo'.
 * @var {number} foo
 */
```

上面的例子等同于下面的示例：

```javascript
/**
 * A variable in the global namespace called 'foo'.
 * @type {number}
 */
var foo;
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @member](http://usejsdoc.org/tags-member.html "tag @member")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>