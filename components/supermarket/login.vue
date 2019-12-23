<template>
  <div id="login">
    <div class="loginBox">
      <div>
        <h1>会员登录</h1>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="请输入用户姓名">
        </div>
        <div class="inputText">
          <span></span>
          <input type="password" placeholder="请输入用户密码">
        </div>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="请输入用户手机">
        </div>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="请输入验证码">
        </div>
        <div class="inputCheck">
          <div class="check">
            <mt-switch>记住密码</mt-switch>
          </div>
          <div @click="findback()">找回密码</div>
        </div>
        <div class="loginButton"><button @click="tip">立即登录</button></div>
        <div class="loginButton mt-60"><button @click="register">注册</button></div>
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
    init() {
      var div = document.getElementById("login");
      console.log(document.body.offsetWidth);
      console.log(div);
      console.log(div.style.width);
    },
    findback(){
      this.$router.push("/findback")
    },
    register(){
      this.$router.push("/register");
    },
    tip(){
      this.$toast("登录成功");
      this.$router.push("/index");
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
