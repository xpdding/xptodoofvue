<template>
  <div>
    <h1>AddP</h1>
    <div>
      <el-row>
        <el-col :span="8">
          <div class="grid-content bg-purple">目前用户：</div>
        </el-col>
        <el-col :span="16">
          <div class="grid-content bg-purple-light">{{submitData.usertid}}</div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="8">
          <div class="grid-content bg-purple">项目名称：</div>
        </el-col>
        <el-col :span="16">
          <div class="grid-content bg-purple-light">
            <el-input placeholder="请输入内容" v-model="submitData.pjname" clearable>
            </el-input>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="8">
          <div class="grid-content bg-purple">项目简介：</div>
        </el-col>
        <el-col :span="16">
          <div class="grid-content bg-purple-light">
            <el-input type="textarea" :rows="2" placeholder="请输入内容" v-model="submitData.pjsome">
            </el-input>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-col :span="8">
          <div class="grid-content bg-purple">预计开始时间和结束开始时间：{{submitData.pjtime}}</div>
        </el-col>
        <el-col :span="16">
          <div class="grid-content bg-purple-light">
            <el-date-picker v-model="submitData.pjtime" type="daterange" align="right" unlink-panels range-separator="至" start-placeholder="开始日期" end-placeholder="结束日期" :picker-options="pickerOptions">
            </el-date-picker>
          </div>
        </el-col>
      </el-row>
      <el-row>
        <el-button type="primary">确认后将检测数据信息正确性并提交项目</el-button>
      </el-row>
    </div>
    <div>
      {{submitData}}
    </div>
  </div>
</template>
<script>
// import { getTAGs } from '../../../Moke/Moke01.js'
export default {
  name: 'AddP',
  data () {
    return {
      submitData: {
        usertid: '',
        pjname: '',
        pjsome: '',
        pjtime: []
      },
      pickerOptions: {
        shortcuts: [
          {
            text: '最近一周',
            onClick (picker) {
              const end = new Date()
              const start = new Date()
              start.setTime(start.getTime() - 3600 * 1000 * 24 * 7)
              picker.$emit('pick', [start, end])
            }
          },
          {
            text: '最近一个月',
            onClick (picker) {
              const end = new Date()
              const start = new Date()
              start.setTime(start.getTime() - 3600 * 1000 * 24 * 30)
              picker.$emit('pick', [start, end])
            }
          },
          {
            text: '最近三个月',
            onClick (picker) {
              const end = new Date()
              const start = new Date()
              start.setTime(start.getTime() - 3600 * 1000 * 24 * 90)
              picker.$emit('pick', [start, end])
            }
          }
        ]
      }
    }
  },
  mounted () {
    this.submitData.usertid = this.$store.state.uinfo.tid
  }
}
</script>
<style scoped>
.el-row {
  margin-bottom: 20px;
}
.el-col {
  border-radius: 4px;
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
</style>
