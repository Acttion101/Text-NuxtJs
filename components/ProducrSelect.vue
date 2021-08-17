<template>
<b-container class="cion" >

</b-container>
</template>
   <script>

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
.cion{
display: flex;
width: 100%;
height: 400px;
align-items: center;
margin-top: 50px;
padding: 10px;
background-color: rgb(199, 130, 1);
margin-bottom: 60px;


}
.btn-cion{
    height: 100px;
    width: 20px;
    background-color: rgb(199, 130, 1);
    font-size: 30px;
}

</style>
