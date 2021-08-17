<template>
<div>
  <b-container>
      <div class="text">
      <h1>จำนวณเงิน: 10 บาท </h1>
      </div>
      <Cion/>
      <b-button to="/" class="btn-ok">ยืนยัน</b-button>
  </b-container>
    
</div>
</template>

<script>
export default {
  layout:"mainLayout"
}
</script>
<style >
.text{
    display: flex;
    width: 100%;
   margin-left: 80%;
   margin-top: 20px;
}
.btn-ok{
  width: 10%;
  height: 50px;
background-color: green;
color: white;
margin-left: 90%;
margin-top: -50px;
font-size: 28px;
}
</style>
