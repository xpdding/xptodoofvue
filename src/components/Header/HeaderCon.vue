<template>
  <div>
    <Menu mode="horizontal" theme="dark" active-name="1">
      <div class="layout-logo">
        <div class="logo-text">OFWEBDEMO</div>
      </div>
      <div class="layout-nav">
        <MenuItem name="1">
        <Icon type="ios-navigate"></Icon>
        TODOMAIN
        </MenuItem>
        <MenuItem name="2">
        <Icon type="ios-keypad"></Icon>
        跑步
        </MenuItem>
        <MenuItem name="3">
        <Icon type="ios-analytics"></Icon>
        个人中心
        </MenuItem>
        <MenuItem name="4">
        <Icon type="ios-paper"></Icon>
        跑步
        </MenuItem>
      </div>
    </Menu>
  </div>
</template>
<script>
export default {
  name: 'HeaderCon',
  data () {
    return {}
  }
}
</script>
<style scoped>
.layout-nav {
  width: 600px;
  margin: 0 auto;
  margin-right: 20px;
}
.logo-text{
  line-height: 100%;
  padding: 10px 2px;
}
.layout-logo {
  width: 100px;
  height: 30px;
  background: #e7b307;
  border-radius: 3px;
  float: left;
  position: relative;
  top: 15px;
  left: 20px;
  color: white;
  /* line-height: 100%; */
}
</style>
