<template>
  <div id="app">
    <!-- <div id="nav"> -->
      <!-- <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> -->
    <!-- </div> -->
      <myheader></myheader>

    <router-view />
  </div>
</template>
<script>
import myheader from './components/header.vue'
  import { obj } from "./utils.js"
  export default {
    components: {
      myheader
    },
    mounted() {
      //挂载完之后去执行这个setrem()
      obj.setRem()
    }
  }
</script>

<style lang="less">
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    padding-bottom:150/100rem;
  }

  /* #nav {
  padding: 30px;
} */

  #nav a {
    font-weight: bold;
    color: #2c3e50;
  }

  #nav a.router-link-exact-active {
    color: #42b983;
  }

  
  body {
    font-size: 16px;
    background: rgba(239, 239, 239);
    position:relative;
  }
</style>