<template>
    <div>
        <h2>用户登录</h2>
        <el-form :label-position="labelPosition" label-width="80px" :model="formDate">
            <el-form-item label="用户名">
                <el-input v-model="formDate.username"></el-input>
            </el-form-item>
            <el-form-item label="密码">
                <el-input v-model="formDate.password"></el-input>
            </el-form-item>
        </el-form>
        <el-button type="primary">主要按钮</el-button>
    </div>
</template>
<script>
export default {
  data () {
    return {
      labelPosition: 'top',
      formDate: {
        uesrname: '',
        password: ''
      }
    }
  }
}
</script>
<style scoped>

</style>

