
<script>
export default {
    data(){
        return{
            name:"Khadija Al Ahyane",
            description1:"I’m a last year Computer Science Engineering student with a mathematical backgroud who’s passionate about technology and problem-solving. Alongside my studies, I'm continuously learning new technologies and applying what I've learned to some projects. In my free time, I'm participating on competitive programming contests .",
            description2:"I like building projects that work towards making people’s lives easier. I’m looking forward to joining a great team where I can grow my skills and collaborate with others and learn from them as a software engineering intern.",
            image:"/git.png"
        }
    }
}
</script>
<template>
<div class="abtMain" id="about">
    <div class="abtTitle"><strong>{{name}}</strong></div>
    <div class="desc1">{{description1}}</div>
    <div class="desc2">{{description2}}</div>
    <a  style="margin-bottom: 5%;" href="https://github.com/khadijalahy1">
<img :src="image" class="aboutimage" alt=""/>
    </a>
    
</div>
</template>
<style>
.abtMain{
    z-index: 2;
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
    background-color: #D9D9D9 ;
    color: #202020;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: large;
    justify-content: center;
    align-items: center;
}
.abtTitle{
    text-align: center;
    font-weight: bolder;
    margin-bottom: 5%;
    margin-top: 9%;
    font-size: x-large;

}
.desc1{
    width: 60%;
    text-align: center;
    margin-bottom: 5%;

}
.desc2{
    width: 60%;
    text-align: center;
    margin-bottom: 5%;
}
.aboutimage{
    width: 6em;
    height: auto;
    margin-bottom: 5%;

}
</style>