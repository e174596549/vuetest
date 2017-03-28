<template>
<div class="todo">
  <h1 v-text="title"></h1>
  <ul>
    <li v-for="item in items" v-text="item.label"></li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'todo',
  data() {
    return {
      title: 'Welcome to Your TODO List',
      items: [{
        label: 'coding',
        isFinished: false
      }, {
        label: 'walking',
        isFinished: false
      }]
    }
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
</style>
