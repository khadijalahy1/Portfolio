<script setup>
import HomeComponent from './components/mainComponents/HomeComponent.vue'
import skillsComponent from './components/mainComponents/skillsComponent.vue';
import ProjectComponent from './components/mainComponents/ProjectComponent.vue';

</script>

<template>
    <div class="main">
        <HomeComponent />
        <skillsComponent />
        <ProjectComponent/>
      
    </div>
</template>

<style>
.main {
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
    padding-left: 0%;

}
*, html {
    margin:0;
    padding:0;  
}
</style>
