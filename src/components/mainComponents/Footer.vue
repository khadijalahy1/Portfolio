<script setup>


</script>
<template>
<div class="footer" id="footer">
    <div class="logos">
        <a href="https://github.com/khadijalahy1"  class="logo"><img src="/github.png" alt="" class="logo"/></a>
        <a href="https://www.linkedin.com/in/khadija-al-ahyane/" class="logo"><img src="/linkedin.png" alt="" class="logo"/></a>

    </div>
    <div class="flinks">
        <a href="#about" class="labelf"> about</a>
        <a href="#contact" class="labelf">contact</a>
        <a href="#resume" class="labelf">Resume</a>
    </div>
</div>

</template>
<style>
.logo{
    width: 2.5em;
    height: 2.5em;
    margin-right: 3%;
}
.labelf{
   
    color: #202020;
    width: 20%;
}
.footer{
    width: 100%;
    height: auto;
    
    background-color:#D9D9D9 ;
    display: flex;
    flex-direction: row;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: large;
    justify-content: center;
    color: #202020;
    padding-bottom: 2%;
  

}
.logos{
    width: 50%;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    padding-left: 5%;
    padding-top: 1.5%;


}

.flinks{
    display: flex;
    flex-direction: row;
    width: 50%;
    align-items: center;
    justify-content: flex-end;
    padding-top: 2%;
    font-size: large;
}


</style>