<template>
  <div id="app">
    <c-header />
    <router-view />
    <c-footer />
  </div>
</template>

<script>
import CHeader from './components/c-header'
import CFooter from './components/c-footer'
export default {
  name: 'App',
  components: {
    'c-header': CHeader,
    'c-footer': CFooter
  }
}
</script>

<style>
  @import url(http://fonts.googleapis.com/css?family=Roboto:400,300,400italic,500,700,100);

  #app {
      font-family: Avenir, Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
  }
</style>