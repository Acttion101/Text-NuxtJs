<template>
<b-container>
   <div class="price">
  <h1>จำนวณเงิน: 5 บาท </h1> </div>
  <b-button to="/inputCoin" class="btn-input">เติมจำนวณเงิน</b-button>

    <div class="container-product" v-for="data in datas" :key="data.id">
       <img :src="data.image" class="photo-item"  />
      <h2>{{ data.name }} </h2>
       <h1>{{ data.price }} บาท</h1>
       <b-button to="/Product" class="btn-product">เลือก</b-button>
   

      
    </div>
</b-container>
</template>

<script>
import axios from '@nuxtjs/axios'
export default {
  layout:"mainLayout",
  data(){
    return{
      datas: []
    }
  },
  async asyncData({$axios}){
    const datas = await $axios.$get('https://www.mocky.io/v2/5c77c5b330000051009d64c9')
    console.log(datas)
    return{datas: datas.data}
    
  }
}
</script>
<style>
.btn-input{
  width: 100%;
  background-color: rgb(199, 130, 1);
  height: 80px;
  text-align: center;
  font-size: 40px;
}
.price{
     display: flex;
    width: 100%;
   margin-left: 80%;
   margin-top: 20px;
}
.btn-product{
  width: 20%;
  height: 50px;
background-color: green;
color: white;
text-align: center;
  font-size: 28px;
  margin-top: -1px;
}
.container-product{
  margin-top: 8px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
