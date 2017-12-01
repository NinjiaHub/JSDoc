# @default

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="Synonyms">同义词</span>

`@defaultvalue`

## <span id="syntax">语法</span>

`@default [<some value>]`

## <span id="overview">概述</span>

`@default` 标签允许给标识符的赋值添加文档注释。你可以自己给该标签提供一个默认值，也可以让 JSDoc 从源码中提取默认值 -- 但是仅限于赋值给标识符的为基本数据类型：数字，字符串，布尔值或者 null。

## <span id="examples">示例</span>

下面的例子给一个常量添加了文档注释。常量的值为 `0xff0000`。通过添加 `@default` 标签，这个默认值也会被自动添加到文档中。

**给常量的数字值添加注释**

```javascript
/**
 * @constant
 * @default
 */
const RED = 0xff0000;
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @default](http://usejsdoc.org/tags-default.html "tag default")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>