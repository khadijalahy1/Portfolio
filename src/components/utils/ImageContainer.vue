
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
<img class="imgContour" :src="path">
</template>
<style>
.imgContour {
  border-radius: 50%;
  border:0.3em solid #FFEE32 ;
  width: 15em;
  height: auto;
  

}
.imgContour:hover{
  opacity: 0.6;
}


</style>