# @ignore

## 内容列表 🕊️

* [概述](#overview "overview")
* [示例](#examples "examples")

## <span id="overview">概述</span>

`@ignore` 标签表示代码中的某个标识符不应该出现在文档中。该标签的优先级高于任何其他标签。

对于大多数 JSDoc 模版(包括默认模版)来说，`@ignore` 标签有以下影响：

* 如果 `@ignore` 标签与 `@module` 标签或者 `@class` 标签一起使用，则整个模块或者整个类都不会出现在生成的文档中；
* 如果 `@ignore` 标签与 `@namespace` 标签一起使用，则必须在每一个子类或者子命名空间的注释中使用 `@ignore` 标签。否则，子类和子命名空间将会出现在生成的文档中，但是名称是不全的(因为父命名空间被使用了 `@ignore` 标签)。

## <span id="examples">示例</span>

下面的例子中,`Jacket` 和 `Jacket#color` 不会出现在生成的文档中：

**类中使用 @ignore 标签**

```javascript
/**
 * @class
 * @ignore
 */
function Jacket() {
    /** The jacket's color. */
    this.color = null;
}
```

下面的例子中，命名空间 `Clothes` 包含一个子类 `Jacket`。`@ignore` 标签必须添加到 `Clothes` 以及 `Clothes. Jacket ` 的文档注释中。`Clothes`, `Clothes.Jacket` 和 `Clothes.Jacket#color` 将不会出现在文档中。

**有子类的命名空间**

```javascript
/**
 * @namespace
 * @ignore
 */
var Clothes = {
    /**
     * @class
     * @ignore
     */
    Jacket: function() {
        /** The jacket's color. */
        this.color = null;
    }
};
```

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @ignore](http://usejsdoc.org/tags-ignore.html "tag @ignore")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>