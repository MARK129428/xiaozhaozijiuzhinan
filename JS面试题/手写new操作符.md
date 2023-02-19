## 手写new操作符

```js
const ObjectFactory = (...args) => {
  const obj = {}
  const Constructor = [].shift.call(args)
  obj.__proto__ = Constructor.prototype
  const ret = Constructor.apply(obj,  args)
  return typeof ret === 'object' ? ret : obj
}
```