<template>
  <div id="shopcar">
    <vueheader></vueheader>
    <div class="shopcarBox">
      <div class="shopcarItem" v-for="(item,i) of data" :key="i">
        <div>
          <img @click="check(i)"  src="../../assets/index/notCheckd.svg" />
        </div>
        <div>
          <img src="../../assets/index/19.jpg" alt />
        </div>
        <div class="shopCarText">
          <div>
            <p>小米Max全网通4G大屏智能手机</p>
            <span>颜色:金色&nbsp;内存:1278G</span>
            <p>2988购物币+700积分</p>
          </div>
          <div>
            <div>
              <div>
                <img src="../../assets/index/jian.png" />
              </div>
              <div>
                <input type="text" value="1" />
              </div>
              <div>
                <img src="../../assets/index/jia.png" />
              </div>
            </div>
            <div>
              <img src="../../assets/index/delete1.svg" alt />
            </div>
          </div>
        </div>
      </div>
    </div>
    <vuefooter></vuefooter>
  </div>
</template>
<style scoped>
@import "./css/shopcar.css";
</style>
<script>
import shopcar from "./common/headerShopcar.vue";
import vuefooter from "./common/footer.vue";
export default {
  data() {
    return {
      data: [
        {
          title: "小米Max全网通4G大屏智能手机",
          color: "金色",
          size: "1287G",
          price: "6299",
          pic: "../../assets/index/19.jpg"
        },
        {
          title: "小米Max全网通4G大屏智能手机",
          color: "金色",
          size: "1287G",
          price: "6299",
          pic: "../../assets/index/19.jpg"
        },
        {
          title: "小米Max全网通4G大屏智能手机",
          color: "金色",
          size: "1287G",
          price: "6299",
          pic: "../../assets/index/19.jpg"
        },
        {
          title: "小米Max全网通4G大屏智能手机",
          color: "金色",
          size: "1287G",
          price: "6299",
          pic: "../../assets/index/19.jpg"
        },
        {
          title: "小米Max全网通4G大屏智能手机",
          color: "金色",
          size: "1287G",
          price: "6299",
          pic: "../../assets/index/19.jpg"
        },
        {
          title: "小米Max全网通4G大屏智能手机",
          color: "金色",
          size: "1287G",
          price: "6299",
          pic: "../../assets/index/19.jpg"
        }
      ],
      footer: [],
      footerFocus: [],
      currentIndex: [
        { isSelect: false },
        { isSelect: false },
        { isSelect: true },
        { isSelect: false }
      ],
      color: [
        { isSelect: "#8a8a8a" },
        { isSelect: "#8a8a8a" },
        { isSelect: "#f58919" },
        { isSelect: "#8a8a8a" }
      ],
      href: ["index", "others", "shopcar", "myself"]
    };
  },
  mounted() {
    this.getIndex();
  },
  methods: {
    getIndex() {
      var url = "/indexs";
      this.axios.get(url, { params: "" }).then(result => {
        for (var key of result.data.data) {
          if (key.type == "footer") {
            this.footer.push(key);
          } else if (key.type == "footer_focus") {
            this.footerFocus.push(key);
          }
        }
      });
    },
    changeState(n) {
      //函数功能:将当前参数下标
      //对应数组值修改true其它修改false
      //1:创建循环,循环数组中内容
      for (var i = 0; i < this.currentIndex.length; i++) {
        //2:判断如果循环下标与n相等 20
        if (n == i) {
          //3:当前下标元素true 10:22
          this.currentIndex[i].isSelect = true;
          this.color[i].isSelect = "#f58919";
          this.$router.push(this.href[i]);
        } else {
          //4:其它元素修改false
          this.currentIndex[i].isSelect = false;
          this.color[i].isSelect = "#8a8a8a";
        }
      }
    },
    check(i) {
      var imgs = document.querySelectorAll(".shopcarItem>div:nth-child(1)>img");
      if(imgs[i].src=="http://127.0.0.1:3000/shopcar/checked.svg"){
        imgs[i].src="http://127.0.0.1:3000/shopcar/notCheckd.svg"
      }else{
        imgs[i].src="http://127.0.0.1:3000/shopcar/checked.svg"
      }
    }
  },
  components: {
    vueheader: shopcar,
    vuefooter: vuefooter
  }
};
</script>