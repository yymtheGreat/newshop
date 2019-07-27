<template>
    <div class="login">
        <el-form :label-position="labelPosition" label-width="80px" :model="formDate" class="login-form">
           <h2>用户登录</h2>
            <el-form-item label="用户名">
                <el-input v-model="formDate.username"></el-input>
            </el-form-item>
            <el-form-item label="密码">
                <el-input v-model="formDate.password"></el-input>
            </el-form-item>
            <el-button type="primary" @click.prevent="handleLogin">主要按钮</el-button>
        </el-form>
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
  },
  methods: {
    handleLogin () {
      console.log(1)
      this.$http.post(`login`, this.formDate).then(res => {
        console.log(res)
        const {data: {data, meta: {msg, status}}} = res
        console.log(data, msg)
        if (status === 200) {
          this.$message(msg)
        } else {
          this.$message.error(msg)
        }
      })
    }
  }
}
</script>
<style scoped>
  .login {
    height: 100%;
    background-color: rgb(35, 86, 226);
    display:flex;
    justify-content: center;
    align-items: center;
   }
  .login-form {
    background-color: white;
    padding: 20px;
    width: 400px;
    border-radius:  5px;
  }
</style>
