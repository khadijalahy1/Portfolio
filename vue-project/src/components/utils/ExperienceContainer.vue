
<script setup>
defineProps({
  date: {
    type: String,
    required: true
  },
  location:{
    type: String,
    required: true
  },
  description:{
    type:String,
    required:true
  },
  linkToOrganization:{
    type:String,

  }
})
</script>

<template>
<div class="experienceTL">
    <div class="experienceItem">{{date}}</div>
    <a class="experienceItem" :href="linkToOrganization" >{{location}}</a>
    <div class="experienceItem">{{description}}</div>

</div>
  
</template>
<style>
.experienceTL{
    width: 100%;
    height:auto;
    margin-left: 5%;
    margin-right: 5%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: large;

}
.experienceItem{
    width: 100%;
    height: auto;
    text-align: center;
}


</style>