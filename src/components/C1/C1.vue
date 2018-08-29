<template>
  <div>
    <h1>C1_FN</h1>
    <div class="t">
      <el-row>
        <el-col :span="24">
          <div class="grid-content bg-purple"><i class="el-icon-menu"></i></div>
        </el-col>
        <!-- <el-col :span="24"><div class="grid-content bg-purple-light"></div></el-col> -->
      </el-row>
      <el-row>
        <!-- <el-col :span="24"><div class="grid-content bg-purple"></div></el-col> -->
        <el-col :span="24">
          <div class="grid-content bg-purple-light"><i class="el-icon-date"></i></div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="24">
          <div class="grid-content bg-purple"><i class="el-icon-success"></i></div>
        </el-col>
        <!-- <el-col :span="24"><div class="grid-content bg-purple-light"></div></el-col> -->
      </el-row>
      <el-row>
        <!-- <el-col :span="24"><div class="grid-content bg-purple"></div></el-col> -->
        <el-col :span="24">
          <div class="grid-content bg-purple-light"><i class="el-icon-star-on"></i></div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="24">
          <div class="grid-content bg-purple"><i class="el-icon-setting"></i></div>
        </el-col>
        <!-- <el-col :span="24"><div class="grid-content bg-purple-light"></div></el-col> -->
      </el-row>
    </div>
  </div>
</template>
<script>
export default {
  name: 'C1'
}
</script>
<style scoped>
.el-row {
  margin-bottom: 20px;
  border:  2px solid red;
  &:last-child {
    margin-bottom: 0;
  }
}
.el-col {
  border-radius: 4px;
  /* margin-top: 100px; */
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
.t {
  /* display: flex;
  flex-direction: row; */
  font-size: 400%;
  color: darkcyan
}
</style>
