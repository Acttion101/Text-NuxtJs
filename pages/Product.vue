<template>
<div>
  <b-container>
      <div class="text">
      <h1>จำนวณเงิน: 10 บาท </h1>
      </div>
    <ProducrSelect/>
      <b-button to="/" class="btn-ok-product">ยืนยันสินค้าสินค้า</b-button>
  </b-container>
    
</div>
</template>

<style >
.text{
    display: flex;
    width: 100%;
   margin-left: 80%;
   margin-top: 20px;
}
.btn-ok-product{
  width: 20%;
  height: 50px;
background-color: green;
color: white;
margin-left: 80%;
margin-top: -50px;
font-size: 28px;
}
</style>
