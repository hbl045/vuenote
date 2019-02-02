<template>
  <div id="app">
    <heads></heads>
    <fnav></fnav>
    <router-view/>
  </div>
</template>

<script>
  import heads from './components/common/header/header.vue'
  import fnav from './components/common/floatnav/floatnav'
export default {
  name: 'App',
  data(){
    return{

    }
  },
  components:{
    heads,
    fnav
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
}
  body {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
  }

</style>
