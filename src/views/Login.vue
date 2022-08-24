<template>
  <div class="login_container">
    <div class="login_box">
      <el-card>
      <el-form :model="ruleForm" status-icon :rules="loginFormRules" ref="ruleFormRef" label-width="100px"
        class="demo-ruleForm">
        <el-form-item label="用户名" prop="username">
          <el-input v-model="loginForm.username"></el-input>
        </el-form-item>
        <el-form-item label="密码" prop="pass">
          <el-input type="password" v-model="loginForm.password"></el-input>
        </el-form-item>
        <el-form-item>
          <el-button type="primary" @click="submitForm('ruleForm')">提交</el-button>
          <el-button @click="resetForm('ruleForm')">重置</el-button>
        </el-form-item>
      </el-form>
    </el-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
      loginForm: {
        username: 'admin',
        password: '123456'
      },
      loginFormRules: {
      }
    }
  },
  methods: {}
}
</script>

<style lang="scss" scoped>
.login_container {
  // background-image: url('../assets/login.png');
  background-color: #ffc9c9;
  width: 100%;
  height: 100%;
  .login_box {
    width: 400px;
    height: 300px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%);
    background-color: #fff;
  }
}
</style>
