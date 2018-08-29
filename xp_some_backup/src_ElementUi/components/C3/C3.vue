<template>
  <div>
    <h1>C3_TAGS</h1>
    <div>
      <el-button type="primary" round>添加一个TAG</el-button>
    </div>
    <div v-for="(tag,index) in pjtagsdata" :key="tag">
      <el-row>
        <el-col :span="24">
          <div class="grid-content" :class="index%2===0?'bg-purple':'bg-purple-light'">
            <span class="pjname-C">{{'#'+tag}}</span>
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
import { getTAGs } from '../../../Moke/Moke01.js'
export default {
  name: 'C3',
  data () {
    return {
      pjtagsdata: []
    }
  },
  mounted () {
    this.pjtagsdata = getTAGs().data
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
