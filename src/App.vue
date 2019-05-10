<template>
  <div id="app">
    <link href='https://fonts.googleapis.com/css?family=Roboto:100,300,400,500,700,900|Material+Icons' rel="stylesheet"/>
    <Header msg="DECAP Database Editor"/>
    <Platforms/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Platforms from './components/Platforms.vue'

export default {
  name: 'app',
  components: {
    Header,
    Platforms
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
</style>
