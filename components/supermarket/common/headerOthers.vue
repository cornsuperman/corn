<template>
<body>
  <header id="header">
    <nav class="nav">
      <div>
        <a href="#"><img src="../../../assets/index/back.png" alt=""></a>
      </div>
      <div>
        <input type="text" placeholder="请输入您要搜索的内容" />
      </div>
      <div>
        <span>三</span>
      </div>
    </nav>
  </header>
</body>
</template>
<style scoped>

/* 头部开始*/
#header {
  width: 100%;
  height: 3.5rem;
  display: flex;
  justify-content: space-between;
  background: #f5f5f5;
  position: fixed;
  top: 0;
  z-index: 10;
}

/* 头部导航栏 */
#header .nav {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-between;
  font-size: 1.5rem;
  position: relative;
}

.nav div:first-child {
  padding: 1rem;
}

.nav div:nth-child(2) {
  width: 80%;
  margin: 0 auto;
  padding: 0.7rem;
  margin-left: -0.4rem;
  text-align: center;
}

.nav div:nth-child(2)>input {
  height: 1.2rem;
  width: 80%;
  padding: 0.4rem 0;
  border: 1px solid #ddd;
  padding-left: 2rem;
  background-image: url(../../../assets/index/search.png);
  background-repeat: no-repeat;
  background-size: 1.5rem;
  background-position: 0 center;
  background-color: #e6e6e6;
  font-size: 1rem;
  border-radius: 0.2rem;
  outline: none;
}

.nav div:last-child {
  padding: 1rem;
}

/* 侧边栏开始*/
.side {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 10;
}

.side ul {
  width: 18.75rem;
  background: #343434;
  margin-left: -18.75rem;
}

.side ul li {
  height: 1rem;
  padding: 1rem;
  border-top: 1px solid #4d4d4d;
  border-bottom: 1px solid #262626;
}

.side ul li a {
  font-size: 1.4rem;
  color: #fff;
}

</style>
<script>
export default {
  methods: {
    side() {
      var ul = document.querySelector(".side");
      ul.style.transition = "all 0.3s linear";
      ul.style.marginLeft = 18.75 + "rem";
    },
    sideNone() {
      var ul = document.querySelector(".side");
      ul.style.transition = "all 0.5s linear";
      ul.style.marginLeft = -18.75 + "rem";
    }
  }
};
</script>