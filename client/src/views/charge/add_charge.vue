<template>
  <div class="app-container">
    <el-form ref="form" :model="form" label-width="120px">
      <el-form-item label="收费项目编号">
        <el-input v-model="form.code" type="name"  placeholder="建议EP开头" />
      </el-form-item>
      <el-form-item label="收费项目名称">
        <el-input v-model="form.name" type="name" />
      </el-form-item>
      <el-form-item label="所属小区编号">
        <el-input v-model="form.name" type="name" />
      </el-form-item>
      <el-form-item label="修改时间">
        <el-col :span="11">
          <el-date-picker v-model="form.add_date" type="date" placeholder="请选择日期" style="width: 100%;" />
        </el-col>
        <el-col :span="2" class="line">-</el-col>
        <el-col :span="11">
          <el-time-picker v-model="form.add_time" type="fixed-time" placeholder="请选择时间" style="width: 100%;" />
        </el-col>
      </el-form-item>
      <el-form-item label="备注">
        <el-input v-model="form.remark" type="desc" />
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="onSubmit">提交</el-button>
        <el-button @click="onCancel">取消</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        code: '',
        name: '',
        status: '',
        community_code: '',
        add_date: '',
        add_time: ''
      }
    }
  },

  methods: {
    onSubmit() {
      this.$message('已提交')
    },
    onCancel() {
      this.$message({
        message: '已取消',
        type: 'warning'
      })
    },
    created() {
    },
    mounted() {
    }
  }
}
</script>

<style scoped>
  .line{
    text-align: center;
  }
</style>
