<template>
<div id="app">
  <mheader></mheader>
</div>
</template>

<script>
import mheader from './components/header/header'

export default {
  name: 'app',
  components: {
    mheader
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
