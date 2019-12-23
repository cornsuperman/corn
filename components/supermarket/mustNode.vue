<template>
  <div id="login">
    <div class="loginBox">
      <div>
        <h1>用户须知</h1>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="用户姓名">
        </div>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="用户密码">
        </div>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="联系电话">
        </div>
        <div class="inputText">
          <span></span>
          <input type="text" placeholder="推荐人姓名">
        </div>
        <div class="loginButton" style="margin-top:2rem" @click="goMustNode"><button>注册</button></div>
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
   goMustNode(){
     this.$messagebox.confirm("注册成功,是否跳转到登录界面?").then((res)=>{
       this.$router.push("/login");
     }).catch(err=>{})
   }
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
