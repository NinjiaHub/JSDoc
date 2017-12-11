# @augments

## 内容列表 🕊️

* [同义词](#Synonyms "Synonyms")
* [语法](#syntax "syntax")
* [概述](#overview "overview")
* [示例](#examples "examples")
* [相关链接](#related "related links")

## <span id="Synonyms">同义词</span>

`@extends`

## <span id="syntax">语法</span>

`@augments <namepath>`

## <span id="overview">概述</span>

`@augments` 和 `@extends` 标签预示一个标识符继承或者将被添加到父标识符。该标签可以用来给基于类或者基于原型链的继承添加文档注释。

在 JSDoc 3.3.0 及其之后的版本中，如果一个标识符继承自多个父标识符，而且多个父标识符中具有同名的成员时，JSDoc 会从 JSDoc 文档注释中的最后一个父标识符取同名成员的注释。

## <span id="examples">示例</span>

下面的例子中，`Duck` 类被定义为 `Animal` 的子类。`Duck` 类的实例和 `Animal` 类具有相同的属性，`speak` 方法是 `Duck` 类实例所独有的。

**给 类/子类 关系添加注释**

```javascript
/**
 * @constructor
 */
function Animal() {
    /** Is this animal alive? */
    this.alive = true;
}

/**
 * @constructor
 * @augments Animal
 */
function Duck() {}
Duck.prototype = new Animal();

/** What do ducks say? */
Duck.prototype.speak = function() {
    if (this.alive) {
        alert('Quack!');
    }
};

var d = new Duck();
d.speak(); // Quack!
d.alive = false;
d.speak(); // (nothing)
```

下面的例子中，`Duck` 类同时继承了 `Flyable` 和 `Animal` 类，两个父类中都定义了 `takeOff ` 方法。因为 `Duck` 类的注释中将 `@augments Bird` 放在了最后，所以 JSDoc 使用 `Bird#takeOff` 的注释来给 `Duck#takeOff` 添加文档注释。

**多继承中的方法同名**

```javascript
/**
 * Abstract class for things that can fly.
 * @class
 */
function Flyable() {
    this.canFly = true;
}

/** Take off. */
Flyable.prototype.takeOff = function() {
    // ...
};

/**
 * Abstract class representing a bird.
 * @class
 */
function Bird(canFly) {
    this.canFly = canFly;
}

/** Spread your wings and fly, if possible. */
Bird.prototype.takeOff = function() {
    if (this.canFly) {
        this._spreadWings()
            ._run()
            ._flapWings();
    }
};

/**
 * Class representing a duck.
 * @class
 * @augments Flyable
 * @augments Bird
 */
function Duck() {}

// Described in the docs as "Spread your wings and fly, if possible."
Duck.prototype.takeOff = function() {
    // ...
};
```

## <span id="related">相关链接</span>

* [@borrows](https://ninjiahub.github.io/JSDoc/docs/tags/borrows "tag @borrows")
* [@class](https://ninjiahub.github.io/JSDoc/docs/tags/class "tag @class")
* [@mixes](https://ninjiahub.github.io/JSDoc/docs/tags/mixes "tag @mixes")
* [@mixin](https://ninjiahub.github.io/JSDoc/docs/tags/mixin "tag @mixin")

## 声明 ⛰️

本文翻译自[JSDoc 3 官方文档 - @augments](http://usejsdoc.org/tags-augments.html "tag augments")。

如有版权问题请联系译者。

侵删。

内容如有不恰当或者错误的地方，敬请斧正。

转载请注明出处。

## Translator Info ✒️

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>