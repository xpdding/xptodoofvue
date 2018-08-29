<template>
  <div>
    <div>
      <el-menu router :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect" background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
        <el-menu-item index="/">处理中心</el-menu-item>
        <el-submenu index="2">
          <template slot="title">菜单</template>
          <el-menu-item index="/reg">注册</el-menu-item>
          <el-menu-item index="/login">登入</el-menu-item>
          <el-menu-item index="/logout">登出</el-menu-item>
          <el-menu-item index="/center">个人中心</el-menu-item>
          <!-- <el-submenu index="2-4">
            <template slot="title">选项4</template>
            <el-menu-item index="2-4-1">选项1</el-menu-item>
            <el-menu-item index="2-4-2">选项2</el-menu-item>
            <el-menu-item index="2-4-3">选项3</el-menu-item>
          </el-submenu> -->
        </el-submenu>
        <!-- <el-menu-item index="3" disabled>消息中心</el-menu-item> -->
        <el-menu-item index="4">
          <a href="https://www.xupeng.vip" target="_blank">转到新网页</a>
        </el-menu-item>
        <el-menu-item index="5">
          <a href="https://www.xupeng.vip" target="_blank">GITHUB地址</a>
        </el-menu-item>

                <el-submenu index="6">
          <template slot="title">添加</template>
          <el-menu-item index="/AddP">项目</el-menu-item>
          <el-menu-item index="/AddT">TAG</el-menu-item>
          <el-menu-item index="/AddL">事件</el-menu-item>
          <!-- <el-menu-item index="/center">个人中心</el-menu-item> -->
          <!-- <el-submenu index="2-4">
            <template slot="title">选项4</template>
            <el-menu-item index="2-4-1">选项1</el-menu-item>
            <el-menu-item index="2-4-2">选项2</el-menu-item>
            <el-menu-item index="2-4-3">选项3</el-menu-item>
          </el-submenu> -->
        </el-submenu>
      </el-menu>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Header',
  data () {
    return {
      activeIndex: '1'
    }
  },
  methods: {
    handleSelect (key, keyPath) {
      console.log(key, keyPath)
    }
  }
}
</script>
<style scoped>
</style>
