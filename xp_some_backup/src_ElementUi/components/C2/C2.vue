<template>
  <div>
    <h1>C2_PJ</h1>
    <div>
      <el-button type="primary" round>添加一个项目</el-button>
    </div>
    <div v-for="(pj,index) in pjdata" :key="pj.pjid">
      <el-row>
        <el-col :span="24">
          <div class="grid-content" :class="index%2===0?'bg-purple':'bg-purple-light'">
            <span class="pjname-C">{{pj.pjname}}</span>
          </div>
        </el-col>
        <!-- <el-col :span="24">
          <div class="grid-content bg-purple-light"></div>
        </el-col> -->
      </el-row>
    </div>
    <div>
      <!-- {{pjdata}} -->
    </div>
  </div>
</template>
<script>
import { getPJs } from '../../../Moke/Moke01.js'
export default {
  name: 'C2',
  data () {
    return {
      pjdata: []
    }
  },
  mounted () {
    this.pjdata = getPJs().data
    console.log(getPJs().data)
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
.pjname-C{
  display: block;
  margin: 0 auto;
  line-height: 100%;
  font-size: 200%;
  font-weight:bold;
  border: 1px solid yellow
}
</style>
