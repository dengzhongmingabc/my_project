<template>
  <div class="login-form">
    <div class="g-form">
      <div class="g-form-line">
        <span class="g-form-label">用户名：</span>
        <div class="g-form-input">
          <input type="text" v-model="username"
                placeholder="请输入用户名">
        </div>
        <span class="g-form-error"></span>
      </div>
      <div class="g-form-line">
        <span class="g-form-label">密码：</span>
        <div class="g-form-input">
          <input type="password" v-model="password" placeholder="请输入密码">
        </div>
        <span class="g-form-error"></span>
      </div>
      <div class="g-form-line">
        <div class="g-form-btn">
          <a class="button" @click="login">登录</a>
        </div>
      </div>
      <p></p>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
        username:'',
        password:''
    }
  },
  methods:{
      login(){
          this.$emit('loginsuccess',{username:this.username})
      }
  }
}
</script>

<style scoped>
</style>

