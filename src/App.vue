<script setup>
import HomeComponent from './components/mainComponents/HomeComponent.vue'
import skillsComponent from './components/mainComponents/skillsComponent.vue';
import ProjectComponent from './components/mainComponents/ProjectComponent.vue';
import TimeLineComponentVue from './components/mainComponents/TimeLineComponent.vue';
import AboutComponent from './components/mainComponents/AboutComponent.vue';
import ContactComponent from './components/mainComponents/ContactComponent.vue';
import FooterVue from './components/mainComponents/Footer.vue';

</script>

<template>
    <div class="main">
        <HomeComponent />
        <skillsComponent />
        <ProjectComponent/>
        <TimeLineComponentVue/>
        <AboutComponent/>
        <ContactComponent/>
        <FooterVue/>
      
    </div>
</template>

<style>
.main {
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
    padding-left: 0%;
    background-color:#D9D9D9 ;

}
*, html {
    margin:0;
    padding:0;  
}
</style>
