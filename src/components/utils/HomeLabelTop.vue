
<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  },
  link:{
    type:String,
    required:true   
  }
})
</script>

<template>
  <a class="label" :href="link">
    {{msg}}
  </a>
</template>
<style>
.label{
    width:10% ;
    height: 10vh;
    text-align: center;
    color:#D6D6D6;
    margin-left: 1%;
    margin-right: 1%;
    background-color:transparent;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;


}
.label:hover{
  color: #FFEE32;
}
</style>