<template>
  <div>
    <h1>C4_LISTS</h1>
<div>
      <el-button type="primary" round>添加一个事件</el-button>
    </div>
    <div v-for="(list,index) in pjlistsdata" :key="list.listid">
      <el-row>
        <el-col :span="20">
          <div class="grid-content" :class="index%2===0?'bg-purple':'bg-purple-light'">
            <span class="pjname-C">{{'>>>'+list.listname}}</span>
          </div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content" :class="index%2===0?'bg-purple':'bg-purple-light'">
            <el-checkbox v-model="list.listchecked">备选项</el-checkbox>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="4">
          <div class="grid-content bg-purple"><span>{{'ID是:'+list.listid}}</span></div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple-light"><span>{{'开始时间:'+list.listft}}</span></div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple"><span>{{'结束时间:'+list.listet}}</span></div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple-light"><span>{{'谁做:'+list.listwhodo}}</span></div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple"><span>{{'标签:'+list.listtags}}</span></div>
        </el-col>
        <el-col :span="4">
          <div class="grid-content bg-purple-light"><span>{{'标※:'+list.listflag}}</span></div>
        </el-col>
      </el-row>
    </div>
    <div>
      <!-- {{pjdata}} -->
    </div>

  </div>
</template>

<script>
import { getLISTs } from '../../../Moke/Moke01.js'
export default {
  name: 'C4',
  data () {
    return {
      pjlistsdata: []
    }
  },
  mounted () {
    this.pjlistsdata = getLISTs().data
  }
}
</script>

<style scoped>
.el-row {
  margin-bottom: 20px;
  border: 2px solid red;
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
  background: #9aa3ad;
}
.bg-purple-light {
  background: #edeff5;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
.pjname-C {
  display: block;
  margin: 0 auto;
  line-height: 100%;
  font-size: 200%;
  font-weight: bold;
  border: 1px solid yellow;
}
</style>
