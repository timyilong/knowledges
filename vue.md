---
tags: [vue]
---


### VUE JS

<hr>

#### vue component & use 区别

<hr>

| Vue.Component           | Vue.Use                |
| ----------------------- | ---------------------- |
| Vue.component()方法注册全局组件 | 接收一个参数                 |
| 第一个参数是自定义元素名称           | 这个参数必须具有install方法      |
| 第二个参数是将要注册的Vue组件        | use函数内部会调用参数的install方法 |

#### vue-cli-service

<hr>

[usage](https://cli.vuejs.org/zh/guide/cli-service.html#%E4%BD%BF%E7%94%A8%E5%91%BD%E4%BB%A4)

<hr>

###### 生产部署

```json
vue-cli-service build
```

<hr>

###### 跨域

#### 组件通信
<hr>

##### 父组件传值到子组件
```json
子组件定义 Props
props:{
    users:{           
      type:Array,
      required:true
    }
  }
父组件传值到 Props 定义的值
<ChildComponent :users="users">
```

##### 父组件调用子组件Method
```json
子组件注册ref
<ChildComponent ref="ref1">
父组件通过ref获取子组件instance

this.$refs.ref1.method1
```

##### 子组件调用父组件Method，且传值到父组件
```json
子组件定义事件，事件绑定到父组件的Method，通过$emit发送到父组件
this.$emit('nameOfChildComponent',{data})

<ChildComponent v-on:nameOfChildComponent="Method Of Parent Component">

Method Of Parent Component 处理子组件的 data
```

##### v-bind v-on
```json
v-bind : 设置 HTML 属性
<v-bind:disabled> = <:disabled>
 v-on : 设置 HTML 事件
<v-on:click> = <@click>
```
