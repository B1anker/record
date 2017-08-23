# 重置transition没效果

## 描述
* 1.去掉transition属性，重置transform
* 2.加回transition属性，设置目标transform
* 3.动画效果不会触发

## 解决
把第2步推入到异步流中
```javascript
this.transition = false
this.tranform = 'reset'
setTimout(() => {
  this.transition = true
  this.tranform = 'target'
})
```