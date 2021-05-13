# 基于 Vue 2 和 Bootstrap 4 的 todo-list demo
> 在线预览 [DEMO](https://duccck.github.io)
## 功能说明
* 新增事件
* 删除事件
* 点击编辑
* 菜单折叠
* 事件状态切换
  * 待完成 -> 已完成
  * 已完成 -> 待完成
* 事件列表切换
  * 待完成列表 <-> 已完成列表
## 代码说明
* methods - 增、删、改及事件处理等功能
* components - 将可复用部分定义为组件，便于在各模块间来回切换渲染
* computed - 用于事件状态变更后的动态计算，将相应状态的内容交给页面渲染
## 难点及解决方法
* 新增属性时，页面内容没有实时渲染更新
  * 原因：在实例创建时，Vue 会为属性创建 setter 和 getter，之后新增的属性没有设置 setter 和 getter，也就无法通知监听器触发页面重新渲染
  * 解决：使用 Vue.set() 为新增属性加上 set 和 get 方法
## 总结
通过这个很简单的项目，发现了很多在看文档时没留意或者被自己轻视的问题和知识点，同时也加深了自己对这些知识点的理解。
