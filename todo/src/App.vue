<template>
<div id="app">
  <todo></todo>
  <city></city>
</div>
</template>

<script>
import todo from './components/todo'
import city from './components/city'

export default {
  name: 'app',
  components: {
    todo,
    city
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
