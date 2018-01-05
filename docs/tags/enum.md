# @enum

## 内容列表 🕊️

* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="syntax">语法</span>

`@enum [<type>]`

## <span id="overview">概述</span>

`@enum` 标签用来标记一组值为相同类型的静态属性。

一个枚举类似于属性的集合，区别就是枚举记录在它自己的文档注释中，而属性是记录在它们的容器的文档注释中。@enum 标签通常和 @readonly 一起使用，因为枚举通常用来表示一组常量。

## <span id="examples">示例</span>

下面的例子展示了如何标记一个表示三种可能状态的对象。注意，枚举的成员可以添加可选的描述。也可以像例子中的成员 'MAYBE' 展示的一样覆盖类型 - 默认情况下枚举成员的类型会被标记为与枚举一致。

**一个表示三种状态的数字枚举**

```javascript
/**
 * Enum for tri-state values.
 * @readonly
 * @enum {number}
 */
var triState = {
    /** The true value */
    TRUE: 1,
    FALSE: -1,
    /** @type {boolean} */
    MAYBE: true
};
```

## <span id="related">相关链接</span>

* [@property](https://ninjiahub.github.io/JSDoc/docs/tags/property "tag @property")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @enum](http://usejsdoc.org/tags-enum.html "tag @enum")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>