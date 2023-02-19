## 手写instanceOf


```js
function instance_of(Obj, Constructor) {
  let implicitPrototype = Obj.__proto__; //获取实例对象的隐式原型
  let displayPrototype = Constructor.prototype; // 获取构造函数的prototype属性
  // while 循环 -> 在原型链上不断向上查找
  while(true) {
    // 知道 imlicitPrototype == null 都没有找到, 返回false
    if (implicitPrototype === null) {
      return false
    } else if (implicitPrototype === displayPrototype) {
      return true
    }
    // 在原型链上不断查找, 构造函数的显示原型
    implicitPrototype = implicitPrototype.__proto__
  }
}
```