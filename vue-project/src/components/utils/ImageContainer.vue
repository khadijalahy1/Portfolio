
<script setup>
defineProps({
  path: {
    type: String,
    required: true
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


</style>