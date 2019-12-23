<template>
<div>
  <!-- <footer id="footer">
      <div class="footerNav">
        <div>
          <a href="#">
            <img src="../../../assets/index/home.svg" alt />
            <p>首页</p>
          </a>
        </div>
        <div>
          <a href="#">
            <img src="../../../assets/index/others.svg" alt />
            <p>分类</p>
          </a>
        </div>
        <div>
          <a href="#">
            <img src="../../../assets/index/shopcar.svg" alt />
            <p>购物车</p>
          </a>
        </div>
        <div>
  <a href="#">-->
  <!-- <img :src="data" /> -->
  <!-- <p>我的</p>
          </a>
        </div>
      </div>
  </footer>-->
  <mt-tabbar class="footer" fixed>
  <mt-tab-item id="首页">
    <img @click="index()" slot="icon" src="../../../assets/index/shouye.png">
    首页
  </mt-tab-item>
  <mt-tab-item id="购物车">
    <img @click="shopcar()" slot="icon" src="../../../assets/index/gouwuchekong.png">
    购物车
  </mt-tab-item>
  <mt-tab-item id="我">
    <img @click="login()" slot="icon" src="../../../assets/index/wo.png">
    我
  </mt-tab-item>
  
</mt-tabbar>
</div>
</template>
<script>
export default {
  
  data(){
    return {
      
    }
  },
  methods: {
    login(){
      this.$router.push("/login")
    },
    index(){
      this.$router.push("/index")
    },
    shopcar(){
      this.$router.push("/shopcar")
    }
  },
  created() {
  }
};
</script>
<style scoped>
/* #footer {
  position: fixed;
  bottom: 0;
  z-index: 10;
  width: 100%;
  background: #fff;
}
#footer .footerNav {
  width: 100%;
  display: flex;
  justify-content: space-around;
}
.footerNav p {
  color: #8a8a8a;
  text-align: center;
} */
.footer{
  width: 100%;
  height:3.5rem;
}
</style>