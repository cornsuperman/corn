<template>
  <div id="myself">
    <mt-tabbar fixed>
      <mt-tab-item
        :focused="currentIndex[i].isSelect"
        v-for="(item,i) of footer"
        :key="i"
        :id="item.id"
        :data-i="i"
        @click.native="changeState(i)"
      >
        <vuefooter :data="currentIndex[i].isSelect?footerFocus[i].src:item.src"></vuefooter>
        <p :style="`color:${color[i].isSelect}`">{{item.name}}</p>
      </mt-tab-item>
    </mt-tabbar>
  </div>
</template>
<style scoped>
@import "./css/myself.css";
</style>
<script>
import vuefooter from "./common/footer.vue"
export default {
  data() {
    return {
      footer: [],
      footerFocus: [],
      currentIndex: [
        { isSelect: false },
        { isSelect: false },
        { isSelect: false },
        { isSelect: true }
      ],
      color: [
        { isSelect: "#8a8a8a" },
        { isSelect: "#8a8a8a" },
        { isSelect: "#8a8a8a" },
        { isSelect: "#f58919" }
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
    }
  },
  components: {
    vuefooter: vuefooter
  }
};
</script>