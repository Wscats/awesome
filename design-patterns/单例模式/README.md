- 1.单例模式的主要思想就是，实例如果已经创建，则直接返回

```js
function creatSingleton() {
    var obj = null
    // 实例如已经创建过，直接返回
    if (!obj) {
        obj = xxx
    }
    return obj
}
```

- 2.符合开放封闭原则