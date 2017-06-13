<template>
  <div id="app">
    <ul>
      <li><router-link to="/first">跳转第一页</router-link></li>
      <li><router-link to="/second">跳转第二页</router-link></li>
    </ul>
    <router-view class="view"></router-view>
  </div>
</template>

<script>
  import firstComponent from './components/firstComponent.vue';
  import secondComponent from './components/secondComponent.vue';
  export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {firstComponent, secondComponent}
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  /*display: inline-block;*/
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
