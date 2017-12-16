# @throws

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="Synonyms">同义词</span>

`@exception`

## <span id="syntax">语法</span>

* `@throws free-form description`
* `@throws {<type>}`
* `@throws {<type>} free-form description`

## <span id="overview">概述</span>

`@throw` 标签用来标记函数可能会抛出的异常。在同一个 JSDoc 注释中可以添加多个 @throw 标签。

## <span id="examples">示例</span>

**使用带类型的 @throws 标签**

```javascript
/**
 * @throws {InvalidArgumentException}
 */
function foo(x) {}
```

**使用带描述的 @throws 标签**

```javascript
/**
 * @throws Will throw an error if the argument is null.
 */
function bar(x) {}
```

**使用带有描述以及类型的 @throws 标签**

```javascript
/**
 * @throws {DivideByZero} Argument x must be non-zero.
 */
function baz(x) {}
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @throws](http://usejsdoc.org/tags-throws.html "tag @throws")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>