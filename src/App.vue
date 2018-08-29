<template>
  <div id="app">
    <div class="t"><Header></Header></div>
    <div class="m"><router-view/></div>
    <div class="b"><Footer></Footer></div>
  </div>
</template>

<script>
import Header from '@/components/Header/Header'
import Footer from '@/components/Footer/Footer'
export default {
  name: 'App',
  components: {
    Header,
    Footer
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
  margin-top: 10px;
}
.t{
  border: 1px solid rgb(4, 235, 204)
}
.m{
  border: 1px solid black
}
.b{
  border: 1px solid blue
}
</style>
