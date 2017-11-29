# @constructs

## 内容列表 🕊️

* [概述](#overview "overview")
* [语法](#syntax "syntax")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="overview">概述</span>

当使用对象字面量定义一个类的时候，可以使用`@constructs`标签给该类中用来构建实例的特定方法添加文档注释。

## <span id="syntax">语法</span>

`@constructs [<name>]`

## <span id="examples">示例</span>

**`@constructs` 标签和 `@lends` 标签一起使用**

```javascript
var Person = makeClass(
    /** @lends Person.prototype */
    {
        /** @constructs */
        initialize: function(name) {
            this.name = name;
        },
        /** Describe me. */
        say: function(message) {
            return this.name + " says: " + message;
        }
    }
);
```

**不使用 @lends 标签时需提供类的名字**

```javascript
makeClass('Menu',
    /**
     * @constructs Menu
     * @param items
     */
    function (items) { },
    {
        /** @memberof Menu# */
        show: function(){
        }
    }
);
```

## <span id="related">相关链接</span>

* [@lends](https://ninjiahub.github.io/JSDoc/docs/tags/lends "tag @lends")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - Using namepaths with JSDoc 3](http://usejsdoc.org/about-namepaths.html "namepaths")。

如有版权问题请联系译者。

侵删。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>