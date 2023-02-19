## 手写apply和call

```js
Function.prototype.callFn = function(context, ...args) {
  args = args || []
  const key = Symbol()
  context[key] = this
  const result = context[key](...args)
  delete context[key]
  return result
}
```


```js
Function.prototype.applyFn = function(context, args) {
  args = args || []
  const key = Symbol()
  context[key] = this
  const result = context[key](...args)
  delete context[key]
  return result
}
```
