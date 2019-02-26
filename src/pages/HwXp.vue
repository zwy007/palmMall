<template>
    <div class="appson">
      <div class="header">
        <img src="../../static/img/mes-yjt.png" alt="" @click="goBack">
        <p>新品</p>
        <span></span>
      </div>

      <div class="div2">
        <ul class="uls">
          <hw-xp-new-product :key="index" v-for="(a,index) in data.products" :data="a"></hw-xp-new-product>
        </ul>
      </div>

      <img class="imgh" src="../../static/img/54022ea0-765a-45ff-82ea-253036f24592.png" alt="">
    </div>
</template>

<script>
  import HwXpNewProduct from "../components/HwXp/HwXpNewProduct"
  import HwWordHeader from "../components/public/HwWordHeader"
  import data from "../api-server/data/xp"
    export default {
        name: "HwXp",
        components:{
          HwXpNewProduct,HwWordHeader
        },
        data(){
          return{
            data
          }
        },
        methods:{
          goBack(){
            this.$router.go(-1);
          }
        }
    }
</script>

<style scoped>
.appson>div{
  padding: .15rem .15rem 0;
  background: white;
}
.appson>.header{
  padding: 0 .2rem;
  height: .45rem;
  background: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.header img{
  width: .13rem; height: .22rem;
}
.header p{
  font-size: .2rem; color: #333;
}
.div2{
  background: white;
}
.uls{
  width: 100%;
  height: 100%;
  overflow-x: hidden;
  overflow-y: auto;
}
.uls>a:nth-child(2n){
  margin-right: 0;
}
.uls>a:nth-child(2n+1){
  margin-right: 2%;
}
  .imgh{
    display: block;
    width: 100%;
    /*padding: 0;*/
    height:.3rem;
    background: #f1f1f1;
  }
</style>
