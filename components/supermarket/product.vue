<template>
    <div class="product_app">
        <div class="good-item" v-for="(item,i) of list" :key="i">
            <img :src="'http://127.0.0.1:3000/'+item.pic" >
            <h4>{{item.lname}}</h4>
            <h5 class="price">{{item.price}}</h5>
            <mt-button @click="addcart" :data-lid="item.lid" :data-lname="item.lname"
            :data-price="item.price"></mt-button>
        </div>
        <mt-button @click="show">查看购物车</mt-button>
        <mt-button size="large" @click="loadMore">加载更多</mt-button>
    </div>
</template>
<script>
export default {
    created(){
        this.loadMore();
    },
    data(){
        return{
            pno:0,
            list:[],
        }
    },
    methods:{
        addcart(e){
            var price=e.target.dataset.price;
            var lname=e.target.dataset.lname;
            var lid=e.target.dataset.lid;
            console.log(price+':'+lname+':'+lid)
            var url="addcart"
            var obj={lid:lid,price:price,lname:lname};
            this.axios.get(url,{params:obj})
            .then(res => {
                console.log(res);
                if(res.data.code==-1){
                    this.$toast("请登录");
                    this.$router.push("/login");
                }else{
                    this.$toast("添加成功");
                }
            })
            .catch(err => {
                console.error(err); 
            })
        },
        loadMore(){
            var url="product"
            this.pno++;
            
        }
    }
}
</script>