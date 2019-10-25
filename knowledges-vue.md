---
tags: [vue]
---

# Knowledges

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
