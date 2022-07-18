<script setup>
defineProps({
  path: {
    type: String,
    required: true
  },
  title:{
    type:String,
    required: true
  },
  description:{
    type:String,
    required:true
  }
})
</script>



<template>
<div class="container">
  <img :src="path" alt="" class="img1">
  <div class="title">{{title}}</div>
  <div class="description">
    {{description}}
  </div>

</div>
</template>
<style>
.img1{
  width:20%;
  height: auto;
}
.container{
  width: 30%;
  height: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.title{
  margin-top: 1%;
  text-align: center;
  color: #FFD100;
  font-size: medium;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;

}
.description{
  width: 70%;
  text-align:justify;
  margin-top: 3%;
  color: #D6D6D6;
  font-size: small;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}


</style>