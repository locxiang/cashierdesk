# 简单收银台 - 微信小程序

## 介绍

此app为简单的收银系统，给航班上不会算账的小姑娘记账使用


## 框架

app基于[wepy](https://tencent.github.io/wepy/)  框架开发

开发风格接近于 Vue.js，支持组件 Props 传值，自定义事件、组件分布式复用Mixin、计算属性函数computed、模板内容分发slot等等
        
>ps: 本人更期待 [mpVue](http://blog.csdn.net/csdnnews/article/details/78252848) , 一个基本完全属于vue风格的小程序框架


## 安装方式

1. `git clone  https://github.com/locxiang/cashierdesk`

2. 进入目录， 执行 `npm install --registry https://registry.npm.taobao.org  `

3. 编译： `npm run dev`

4. 打开`微信开发工具` 选中目录 cashierdesk/dist  

5. 关闭 `微信开发工具` 的4个功能 ： es6转es5， 上传代码时样式补全， 代码自动压缩， 不校验域名


## 坑

### 1. 不要用循环渲染组件，不要用循环渲染组件，不要用循环渲染组件，不要用循环渲染组件
> 因为循环渲染数据之间会相互干扰

### 2. project.config.json文件，中appid修改成自己的

### 3. {{ }} 中只能放入 data 和 computed ，不支持 methods  也不支持函数， vue的朋友注意了

### 4. input是单向数据绑定  没有v-model这样的产物， 可以参考我写的input