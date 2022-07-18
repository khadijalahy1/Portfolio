<script setup >

defineProps({
  image: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  }
});
</script>

<template>

  <div class="containerp">
    
    <img :src="image" alt="" class="pimage" />


    <div class="titleP">{{ title }}</div>

  </div>
</template>
<style>


.imageProject{
  position: absolute;
  top: 0%;
  width: 100%;
  height: 60vh;
  

}


.containerp {
  width: 25%;
  margin-right: 2%;
  margin-bottom: 2%;
  margin-top: 2%;

  height: 40vh;
  background-color: #202020;

}

.pimage {
 width: 100%;
 height:30vh
}
.pimage:hover{
  opacity: 30%;
}

.titleP {
  top: 60vh;
  width: 100%;
  height: 10vh;
  color: #FFD100;
  text-align: center;
  background-color: #202020;
  justify-content: center;
  padding-top: 3%;
  align-items: center;
  font-size: large;
  font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}

</style>