
<script setup>
defineProps({
  path: {
    type: String,
    required: true
  },
  size:{
    type:Number,
    required:true
  }
})
</script>



<template>
<img class="imgContours" :src="path">
</template>
<style>
.imgContours {
  border-radius: 50%;
  border:0.2em solid #FFEE32 ;
  width: 6em;
  height: 6em;
  z-index: 2;

}


</style>