<template>
<div class="hello">
  <h1>{{ msg }}</h1>
  <button v-on:click=" click ">{{message | doSomething}}</button>
</div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  props: ['message'],
  methods: {
    click: function () {
      console.log(this.message);
    }
  },
  filters: {
    doSomething: function (value) {
      // 返回处理后的值
      return value + '-world'
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
