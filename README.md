# vue

vue 是一个款国人编写的 web 前端框架，优点是轻量级，响应式，可双向绑定，组件化，学习曲线平稳，中文文档相当友好，有相当多类似 Element UI 的优秀开源资源，配合全家桶可以比较快速的进行完整项目的开发。缺点是绝大多数功能均可用原生或 jq 实现，自身执行效率并不是很高，全家桶工具庞杂

## cli 脚手架工具

自动实现项目框架，支持 webpack 打包，router，eslint 等等，并提供本地服务器实现代码实时显示更新

- 生成 vue init webpack <my-project>
- 启动 npm run dev

## 常用功能

- bind 绑定 DOM 元素属性

```javascript
<span v-bind:title="message">
      鼠标悬停几秒钟查看此处动态绑定的提示信息！
    </span>
```

- if 条件显示

```javascript
<div id="app-3">
  <p v-if="seen">现在你看到我了</p>
</div>
```

- for 循环 可嵌套 if / for 使用

```javascript
<div id="app-4">
  <ol>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>
  </ol>
</div>

var app4 = new Vue({
  el: '#app-4',
  data: {
    todos: [
      { text: '学习 JavaScript' },
      { text: '学习 Vue' },
      { text: '整个牛项目' }
    ]
  }
})
```

- on 事件绑定监听 类似于 jq

```javascript
<div id="app-5">
  <p>{{ message }}</p>
  <button v-on:click="reverseMessage">逆转消息</button>
</div>
var app5 = new Vue({
  el: '#app-5',
  data: {
    message: 'Hello Vue.js!'
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  }
})
```

- computed

```javascript
<div id="example">
  <p>Original message: "{{ message }}"</p>
  <p>Computed reversed message: "{{ reversedMessage }}"</p>
</div>
var vm = new Vue({
  el: '#example',
  data: {
    message: 'Hello'
  },
  computed: {
    // a computed getter
    reversedMessage: function () {
      // `this` points to the vm instance
      return this.message.split('').reverse().join('')
    }
  }
})
```
