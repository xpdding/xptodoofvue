<template>
  <div id="app">
    <div class="t">
      <el-row>
        <el-col :span="12">
          <div>
            <Header></Header>
          </div>
        </el-col>
        <el-col :span="12">
          <div>
            <HeaderRig></HeaderRig>
          </div>
        </el-col>
      </el-row>
      <!-- <div class="t-1">
        <Header></Header>
      </div>
      <div class="t-2">
        <HeaderRig></HeaderRig>
      </div> -->
    </div>
    <div class="m">
      <router-view/>
    </div>
    <div class="b">
      <Footer></Footer>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header/Header'
import HeaderRig from '@/components/Header/HeaderRig'
import Footer from '@/components/Footer/Footer'
export default {
  name: 'App',
  components: {
    Header,
    Footer,
    HeaderRig
  }
}
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
}
.t {
  border: 1px solid rgb(4, 235, 204);
  display: flex;
  flex-direction: column;
}
.m {
  border: 1px solid black;
}
.b {
  border: 1px solid blue;
  /* position: absolute;  */
  /*相对于父元素contanier定位*/
  width: 100%;
  /* bottom: 0; */
  /*始终距离它的父元素的底部为0px.则是处于父元素的最底*/
}
.t-1 {
  width: 600px;
  border: 1px solid blue;
}
.t-2 {
  width: 600px;
  border: 1px solid blue;
}
</style>
