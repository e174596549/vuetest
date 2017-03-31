<template>
<div class="todo">
  <h1 v-text="title"></h1>
  <ul>
    <li v-for="item in items" v-text="item.label" v-bind:class="{ active: item.isFinished }"></li>
  </ul>
  <hello message='hello'></hello>
</div>
</template>

<script>
import hello from './Hello'
export default {
  name: 'todo',
  data() {
    return {
      title: 'Welcome to Your TODO List',
      items: [{
        label: 'coding',
        isFinished: true
      }, {
        label: 'walking',
        isFinished: false
      }]
    }
  },
  components: {
    hello
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

.active {
  border-bottom-color: inherit;
  border-bottom-style: solid;
  border-bottom-width: 1px;
}
</style>
