<template>
    <div>
        <vueheader></vueheader>
        <div class="cart">
            <div class="selectAll">
                全选<input type="checkbox">
            </div>
            <div class="cart-item" v-for="(item,i) of list" :key="i">
                <div class="lefttxt">
                    <input type="checkbox" v-model="item.cb">
                    <div class="lname">{{item.lname}}</div>
                    <div class="price">{{item.price}}</div>
                </div>
                <mt-button @click="del" :data-id="item.id">删除</mt-button>
            </div>
        </div>
        <div>
            购物车数量
            <span>0</span>
            <mt-button @click="delItem" >删除选中商品</mt-button>
            <mt-button @click="delAll">清空购物车</mt-button>
        </div>
        <vuefooter></vuefooter>
    </div>
</template>
<script>
import vueheader from "./common/header"
import vuefooter from "./common/footer"
export default {
    created(){
        this.loadMore();
    },
    data(){
        return{
            list:[]
        }
    },
    methods:{
        delAll(){
            this.$messagebox.confirm('是否删除指定数据').then(res=>{
                var str="";
                for(var item of this.list){
                    str+=item.id+",";
                }
                if(str.length==0){
                    this.$messagebox("您的购物车为空");
                    return 
                }
                str=str.substring(0,str.length-1);
                var url="delm";
                var obj={ids:str};
                this.axios.get(url,{params:obj}).then(res=>{
                    this.$toast("删除成功");
                    this.loadMore()
                }).catch(err=>{

                })
            })
            .catch(err=>{})
        },
        delItem(){
            this.$messagebox.confirm("是否删除指定数据?").then(res=>{
                var str="";
                for(var item of this.list){
                    if(item.cb){
                        str+=item.id+","
                    }
                }
                if(str.length==0){
                    this.$messagebox("请选择需要删除的商品");
                    return
                }
                str=str.substring(0,str.length-1);
                var url="delm";
                var obj={ids:str};
                this.axios.get(url,{params:obj})
                .then(res=>{
                    this.$toast("删除成功");
                    this.loadMore();
                })
                .catch(err=>{
                    console.log(err)
                })
            })
            .catch(err=>{
                console.log(err)
            })
        },
        del(e){
            this.$messagebox.confirm("是否删除指定商品?")
            .then(res=>{
                var id=e.target.dataset.id;
                var url="del";
                var obj={id:id}
                this.axios.get(url,{params:obj}).then(res=>{
                    if(res.data.code==-2){
                        this.$router.push("/login");
                    }else if(res.data.code==-1){
                        this.$toast("删除失败")
                    }else{
                        this.$toast("删除成功");
                        this.loadMore()
                    }
                })
                .catch(err=>{
                    console.log(err)
                })
            })
            .catch(err=>{
                console.log(err)
            })
        },
        loadMore(){
            var url="findcart";
            this.axios.get(url).then(res=>{
                var rows=res.data.data;
                for(var item of rows){
                    item.cd=false;
                }
                this.list=rows;
            
            })
            .catch(err=>{
                console.log(err)
            })
        }
    },
    components:{
        vueheader,
        vuefooter
    }  
}
</script>
<style scoped>
    .cart-item{
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom:1px solid #ccc;
        margin-top:25px; 
    }
    .lefttxt{
        display: flex;
        align-items:center;
    }
    .price{
        color:red;
        font-size:18px;
        margin-left:15px;
    }
</style>