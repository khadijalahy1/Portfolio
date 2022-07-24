<script  setup>
import HomeLabelTop from '../utils/HomeLabelTop.vue'
import ImageContainer from '../utils/ImageContainer.vue'
</script>
<script>
export default { 
  data() {
    return {
      windowWidth: window.innerWidth,
      path:"me.jpeg",
      sizeImg:15,
      labels:[
        {title:"ABOUT",link:"#about"},
        {title:"SKILLS",link:"#skills"},
        {title:"PROJECTS",link:"#projects"},
        {title:"TIMELINE",link:"#timeline"},
        {title:"RESUME",link:"#resume"}
      ],
      name:"Khadija Al Ahyane",
      greeting:"Welcome To My Portfolio"
    }
  } 
  ,

  mounted() {
    this.$nextTick(() => {
      window.addEventListener('resize', this.onResize);
    })
  },

  beforeDestroy() { 
    window.removeEventListener('resize', this.onResize); 
  },

  methods: {  
    onResize() {
      this.windowWidth = window.innerWidth
    }

    
  } 
}

</script>




<template>
<div class="homePageDiv" id="home">
    <div class="home"> 
        
  </div>
  <div class="mask">
    <div  class="navbar">
      <div class="name">{{name}}</div>
      <div  v-if="windowWidth>840" class="items">
        <HomeLabelTop v-for="label in labels" :msg="label.title" :link="label.link" />
      </div>
    </div>
  
    <div class="me">
      <ImageContainer path="/me.jpeg"  :size=sizeImg />
      <div class="name2">{{name}}</div>
      <div class="descriptionP">{{greeting}}</div>
    </div>
  </div>



</div>

  

</template>

<style>
.homePageDiv{
  width: 100%;
  height: 100vh;
}


.name2{

    margin-top: 5%;
    width:100%;
    height:10vh;
    color: #FFEE32;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-weight: bold;
    font-size: x-large;
    text-align: center;
  

}


.descriptionP{

    margin-top: 5%;
    width:50%;
    height:10vh;
    color: #D6D6D6;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-weight:lighter;
    font-style: italic;
    font-size:xx-large;
    text-align: center;
  

}

.mask {
            position:absolute;
            top:0px;left: 0px;right:0px;bottom: 0px;
            width: 100%;
            height:100vh;
            background: rgba(0, 0, 0, 0.78);
            
        }
.me{
    position: absolute;
    left: 20%;
    right: 20%;
    top:20%;
    display: flex;
    flex-direction: column;
  align-items: center;
  justify-content: center;
    

}
.items{
    position: absolute;
    right: 0%;
    display:flex;
    top:2%;
    flex-direction:row;
    align-self:flex-end;
    padding-left: 0%;
    justify-content: flex-end;
    width: 80%;

}
.name{
    position: absolute;
    left:3%;
    top: 2%;
    width:20%;
    height:100vh;
    color: #FFEE32;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-weight: bold;
    font-size: large;
}
.navbar{
    width:100%;
    height:10vh;
    background-color: transparent;

}
.home{
    position:absolute;
    top:0px;left: 0px;right:0px;bottom: 0px;
    width:100%;
    height:100vh;
    background-image: url('@/assets/pictures/bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
  
}



</style>

