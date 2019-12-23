<template>
<body>
  <div class="body">
    <vueheader></vueheader>
    <section id="section">
      <!-- <div class="banner">
        <div>
          <ul>
            <li>
              <img src="../../assets/index/banner.jpg" alt />
            </li>
            <li>
              <img src="../../assets/index/banner2.jpg" alt />
            </li>
          </ul>
        </div>
      </div> -->
      <mt-swipe :auto="2000" :show-indicators="false"     class="swipe" style="width:100%;height:14rem;margin-bottom:3px">
        <mt-swipe-item><img src="../../assets/index/banner.jpg" alt=""></mt-swipe-item>
        <mt-swipe-item><img src="../../assets/index/banner2.jpg" alt /></mt-swipe-item>
        <mt-swipe-item><img src="../../assets/index/banner2.jpg" alt /></mt-swipe-item>
      </mt-swipe>
      <div class="sectionNav">
        <ul>
          <li>
            <a href="#">
              <img src="../../assets/index/icon1.png" alt />
            </a>
            <p>销量排行</p>
          </li>
          <li>
            <a href="#">
              <img src="../../assets/index/icon2.png" alt />
            </a>
            <p>联盟商家</p>
          </li>
          <li>
            <a href="#">
              <img src="../../assets/index/icon3.png" alt />
            </a>
            <p>最多收藏</p>
          </li>
          <li>
            <a href="#">
              <img src="../../assets/index/icon4.png" alt />
            </a>
            <p>最热搜索</p>
          </li>
        </ul>
      </div>
      <div class="sectionText">
        <p>新闻公告:</p> 
        <!-- <div>
          <ul>
            <li>黑色星期五超级特惠</li>
            <li>水果生鲜限时折扣</li>
            <li>手机数码全场9.9折</li>
            <li>欢度双十二限时抢券</li>
            <li>本商城一部分商品免费</li>
          </ul>
        </div> -->
        <mt-swipe :auto="2500" :show-indicators="false" style="width:100%px;height:3rem">
       <mt-swipe-item><div>黑色星期五超级特惠</div></mt-swipe-item>
        <mt-swipe-item><div>水果生鲜限时折扣</div></mt-swipe-item>
        <mt-swipe-item><div>手机数码全场9.9折</div></mt-swipe-item>
        <mt-swipe-item><div>欢度双十二限时抢券</div></mt-swipe-item>
        <mt-swipe-item><div>本商城一部分商品免费</div></mt-swipe-item>
      </mt-swipe>
        <p>
          <a href="#">
            <span>更多</span>
          </a>
        </p>
      </div>
      <div class="fineProduct">
        <div class="proTitle">
          <samp>
            精品任选
            <span></span>
          </samp>
        </div>
        <div class="proImg">
          <ul>
            <li>
              <a href="#">
                <img src="../../assets/index/1.jpg" alt />
              </a>
            </li>
            <li>
              <a href="#">
                <img src="../../assets/index/2.jpg" alt />
              </a>
            </li>
          </ul>
        </div>
        <div class="proTitle">
          <samp>
            热卖推荐
            <span></span>
          </samp>
        </div>
        <div class="hot">
          <div>
            <div class="productText">
              <p>天天特惠</p>
              <p>每天10点,爆款抢不停</p>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/3.jpg" alt />
              </a>
            </div>
          </div>
          <div>
            <div class="productText">
              <p>生鲜品质日</p>
              <p>优质新鲜 放心好食材</p>
            </div>
            <div>
              <a href="#">
                <img style="height:200px" src="../../assets/index/111.jpg" alt />
              </a>
            </div>
          </div>
        </div>
        <div class="proTitle">
          <samp>
            每周上新
            <span></span>
          </samp>
        </div>
        <div class="newWeek">
          <div>
            <div>
              <div>
                <div class="productText">
                  <p>新机首发</p>
                  <p>有新机更有范</p>
                </div>
              </div>
              <div>
                <a href="#">
                  <img src="../../assets/index/6.jpg" alt />
                </a>
              </div>
            </div>
            <div>
              <div>
                <div class="productText">
                  <p>时令生鲜</p>
                  <p>冬季进补要吃鱼</p>
                </div>
              </div>
              <div>
                <a href="#">
                  <img src="../../assets/index/20.jpg" alt />
                </a>
              </div>
            </div>
          </div>
          <div>
            <div>
              <div class="productText">
                <p>官方正版</p>
                <p>限时抢购正品泰迪熊</p>
              </div>
              <div style="width:121.88px;height:121.88px">
                <img  style="width:100%;height:100%" src="../../assets/index/7.jpg" />
              </div>
            </div>
            <div>
              <div class="productText">
                <p>国行来袭</p>
                <p>任天堂国行版switch买酒送</p>
              </div>
              <div>
                <img src="../../assets/index/switch.jpg" />
              </div>
            </div>
            <div>
              <div class="productText">
                <p>玩转3C</p>
                <p>明星主机,4K体验</p>
              </div>
              <div>
                <img src="../../assets/index/ps4.jpg" />
              </div>
            </div>
          </div>
        </div>
        <div class="proTitle">
          <samp>
            主题馆
            <span></span>
          </samp>
        </div>
        <div class="others">
          <div>
            <div>
              <div class="productText">
                <p>天天特惠</p>
                <p>每天10点,爆款抢不停</p>
              </div>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/10.jpg" />
              </a>
            </div>
          </div>
          <div>
            <div>
              <div class="productText">
                <p>天天特惠</p>
                <p>每天10点,爆款抢不停</p>
              </div>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/8.jpg" />
              </a>
            </div>
          </div>
          <div>
            <div>
              <div class="productText">
                <p>天天特惠</p>
                <p>每天10点,爆款抢不停</p>
              </div>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/11.jpg" />
              </a>
            </div>
          </div>
          <div>
            <div>
              <div class="productText">
                <p>天天特惠</p>
                <p>每天10点,爆款抢不停</p>
              </div>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/12.jpg" />
              </a>
            </div>
          </div>
          <div>
            <div>
              <div class="productText">
                <p>天天特惠</p>
                <p>每天10点,爆款抢不停</p>
              </div>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/13.jpg" />
              </a>
            </div>
          </div>
          <div>
            <div>
              <div class="productText">
                <p>天天特惠</p>
                <p>每天10点,爆款抢不停</p>
              </div>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/14.jpg" />
              </a>
            </div>
          </div>
          <div>
            <div>
              <div class="productText">
                <p>天天特惠</p>
                <p>每天10点,爆款抢不停</p>
              </div>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/15.jpg" />
              </a>
            </div>
          </div>
          <div>
            <div>
              <div class="productText">
                <p>天天特惠</p>
                <p>每天10点,爆款抢不停</p>
              </div>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/16.jpg" />
              </a>
            </div>
          </div>
          <div>
            <div>
              <div class="productText">
                <p>天天特惠</p>
                <p>每天10点,爆款抢不停</p>
              </div>
            </div>
            <div>
              <a href="#">
                <img src="../../assets/index/17.jpg" />
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
  <vuefooter></vuefooter>
</body>
</template>
<style scoped>
@import "./css/index.css";
@import "../../../node_modules/mint-ui/lib/style.css";
</style>
<script>
import vuefooter from "./common/footer.vue";
import vueheader from "./common/header.vue";
export default {
  mounted() {
    
  },
  data() {
    return {
      footer: [],
      footerFocus: [],
      currentIndex: [
        { isSelect: true },
        { isSelect: false },
        { isSelect: false },
        { isSelect: false }
      ],
      color: [
        { isSelect: "#f58919" },
        { isSelect: "#8a8a8a" },
        { isSelect: "#8a8a8a" },
        { isSelect: "#8a8a8a" }
      ],
      href:["index","others","shopcar","myself"]
    };
  },
  methods: {
    // banner() {
    //   var father = document.querySelector("#section .banner>div");
    //   var ul = father.childNodes[0];
    //   var li = ul.children;
    //   var i = 0;
    //   var time = 1000;
    //   var length = li.length - 1;
    //   setInterval(function() {
    //     if (i < length) {
    //       i += 1;
    //       ul.className = "transition";
    //       ul.style.marginLeft = -25.875 * i + "rem";
    //     } else {
    //       i = 0;
    //       ul.className = "";
    //       ul.style.marginLeft = 0;
    //     }
    //   }, time);
    // },
    // bannerText() {
    //   var father = document.querySelector("#section .sectionText>div");
    //   var ul = father.childNodes[0];
    //   var li = ul.children;
    //   var i = 0;
    //   var time = 2000;
    //   var length = li.length - 2;
    //   setInterval(function() {
    //     if (i <= length) {
    //       i += 1;
    //       ul.className = "transition";
    //       ul.style.marginLeft = -14 * i + "rem";
    //     } else {
    //       i = 0;
    //       ul.className = "";
    //       ul.style.marginLeft = 0;
    //     }
    //   }, time);
    // },
  },
  components: {
    vuefooter: vuefooter,
    vueheader: vueheader
  }
};
</script>