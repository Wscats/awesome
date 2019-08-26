# 工厂模式

工厂模式中，我们在创建对象时不会对客户端暴露创建逻辑，并且是通过使用一个共同的接口来指向新创建的对象，用工厂方法代替new操作的一种模式。

```js
class Creator {
    create(name) {
        return new Animal(name)
    }
}

class Animal {
    constructor(name) {
        this.name = name
    }
}

var creator = new Creator()

var duck = creator.create('Duck')
console.log(duck.name) // Duck

var chicken = creator.create('Chicken') 
console.log(chicken.name) // Chicken
```

- 构造函数和创建者分离，对new操作进行封装
- 符合开放封闭原则
