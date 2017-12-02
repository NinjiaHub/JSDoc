# @lends

## 内容列表 🕊️

* [概述](#overview "overview")
* [语法](#syntax "syntax")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="overview">概述</span>

`@lends` 标签允许给对象字面量的所有成员添加文档注释，就像它们(成员)是具有给定名称的符号的成员一样。这在将对象字面量传给一个根据该对象属性创建命名类的方法时非常有用。

## <span id="syntax">语法</span>

`@lends <namepath>`

## <span id="examples">示例</span>

在下面的例子中，通过帮助函数创建一个 `Person` 类，并且该类有两个实例方法 `initialize` 和 `say`。这跟一些流行框架中创建类的方式是相似的。

**示例类**

```javascript
// We want to document this as being a class
var Person = makeClass(
    // We want to document these as being methods
    {
        initialize: function(name) {
            this.name = name;
        },
        say: function(message) {
            return this.name + " says: " + message;
        }
    }
);
```

如果没有注释，JSDoc 不会识别出上面的代码是创建类一个有两个方法的 `Person` 类。要给方法添加文档注释，需要在对象字面量前的文档注释中使用 `@lends` 标签。`@lends` 标签会告诉 JSDoc 对象字面量的所有方法都会被“**借给**” `Persion`变量。同时也需要给对象字面量中的方法分别添加注释。

**标注为静态方法**

```javascript
/** @class */
var Person = makeClass(
    /** @lends Person */
    {
        /**
         * Create a `Person` instance.
         * @param {string} name - The person's name.
         */
        initialize: function(name) {
            this.name = name;
        },
        /**
         * Say something.
         * @param {string} message - The message to say.
         * @returns {string} The complete message.
         */
        say: function(message) {
            return this.name + " says: " + message;
        }
    }
);
```

现在 `initialize` 方法和 `say` 方法都添加了文档注释，但是是做为 `Person` 类的静态方法。这或许正是你想要的，但是在这个例子中，我们想让 `initialize` 方法和 `say` 方法出现在 `Person` 类的实例中。

**标注为实例方法**

```javascript
/** @class */
var Person = makeClass(
    /** @lends Person.prototype */
    {
        /**
         * Create a `Person` instance.
         * @param {string} name - The person's name.
         */
        initialize: function(name) {
            this.name = name;
        },
        /**
         * Say something.
         * @param {string} message - The message to say.
         * @returns {string} The complete message.
         */
        say: function(message) {
            return this.name + " says: " + message;
        }
    }
);
```

最后一步：类框架使用 `initialize` 方法构建 `Person` 类的实例，但是实例中并不需要该方法。解决办法就是给 `initialize` 方法添加 `@constructs` 标签。最后记得移除 `@class` 标签，否则会出现两个被添加了文档注释的类。

```javascript
var Person = makeClass(
    /** @lends Person.prototype */
    {
        /**
         * Create a `Person` instance.
         * @constructs
         * @param {string} name - The person's name.
         */
        initialize: function(name) {
            this.name = name;
        },
        /**
         * Say something.
         * @param {string} message - The message to say.
         * @returns {string} The complete message.
         */
        say: function(message) {
            return this.name + " says: " + message;
        }
    }
);
```

## <span id="related">相关链接</span>

* [@borrows](https://ninjiahub.github.io/JSDoc/docs/tags/borrows "tag @ borrows")
* [@constructs](https://ninjiahub.github.io/JSDoc/docs/tags/constructs "tag @ constructs")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - Using namepaths with JSDoc 3](http://usejsdoc.org/about-namepaths.html "namepaths")。

如有版权问题请联系译者。

侵删。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>