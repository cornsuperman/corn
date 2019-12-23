<template>
  <div id="login">
    <div class="loginBox">
      <div>
        <h1>密码找回</h1>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="请输入用户姓名">
        </div>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="请输入手机号">
          <button>获取验证码</button>
        </div>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="请输入验证码">
        </div>
        <div class="loginButton"><button @click="login">获取新密码</button></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  created() {
    // this.init()
  },
  data() {
    return {
      bool:true
    };
  },
  methods: {
    
   
    login(){
      this.$toast("找回成功");
      this.$router.push("/login");
    },
  },
  computed: {},
  watch: {
    width: function() {
      console.log(document.body.offsetWidth);
      return document.body.offsetWidth + "px";
    },
    height: function() {
      console.log(window.innerHeight);
      return window.innerHeight;
    }
  }
};
</script>

<style scoped>
@import "./css/login.css";

</style>
