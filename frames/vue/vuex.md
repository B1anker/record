## 问题1：使用vuex的mapState导致内存泄漏

## 解决方案：
1.`mapState`中必须使用纯函数。
2.数组的`map`，`filter`，`forEach`等方法，如果数组中的每个值是一个对象，那么操作的时候就必须要小心，不然就会改变原数组的值，从而导致内存泄漏。