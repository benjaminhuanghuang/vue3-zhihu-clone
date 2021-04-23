第3章 初识 Vue3.0： 新特性详解 试看
首先浏览 vue3 新带来的变化，然后从为什么会有 vue3 引出话题， 带领大家学习 compostion API，自定义Hooks，Teleport，Suspense 和 全局 API 修改等一系列 vue3 的重大更新。

共 20 节 (137分钟) 收起列表

## 3-1 vue3 新特性巡礼 (04:45)

## 3-2 为什么会有 vue3 (07:09)

## 3-3 使用 vue-cli 配置 vue3 开发环境 (08:42)
```
  npm i -g @vue/cli

  vue --version

  vue create vue3-basic
```

```
  vue ui
```
## 3-4 项目文件结构分析和推荐插件安装 (08:53)
Instell vs code extension Vetur


## 3-5 vue3 - ref 的妙用 (08:20)试看

## 3-6 更近一步 - reactive (10:14)
```
  toRefs(obj)
```
## 3-7 vue3 响应式对象的新花样 (06:51)
```
  Object.defineProperty(data, 'count', {
    get(){},
    set(){}
  })
```

```
  new Proxy(data, {
    get(){},
    set(key, value){}
  })
```
## 3-8 老瓶新酒 - 生命周期 (07:00)

## 3-9 侦测变化 - watch (07:16)

## 3-10 vue3 模块化妙用- 鼠标追踪器 (09:04)

## 3-11 模块化难度上升 - useURLLoader (09:40)

## 3-12 模块化结合typescript - 泛型改造 (08:28)

## 3-13 Typescript 对 vue3 的加持 (05:48)

## 3-14 Teleport - 瞬间移动 第一部分 (05:47)

## 3-15 Teleport - 瞬间移动 第二部分 (09:16)

## 3-16 Suspense - 异步请求好帮手第一部分 (05:10)

## 3-17 Suspense - 异步请求好帮手第二部分 (06:31)

## 3-18 全局 API 修改 (07:13)

## 3-19 作业节
## 3-20 作业节