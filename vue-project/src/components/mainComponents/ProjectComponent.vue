<script  setup>
import projectContainer from '../utils/projectContainer.vue';
import VueModelProject from '../utils/VueModelProject.vue';

</script>

<script>
export default {

    data(){
        return{
            title:"PROJECTS",
            show:false,
            open: false,
            description:"Some of the projects I've worked on ...",
            textUpdate:"In my free time, I continue to work on personal projects and have many ideas just waiting to be realized.",
            callToGit:"To see more visit my github profile",
            projects:[
                [
                    {title:"Data4everyone",path:'/nasa.PNG',
                    description:"Data4everyone  is a project built during Nasa Space Apps Challenge Hackathon . It’s a web app that aims to guide each user through his journey of searching for data until he’ll find the one that will meet exactly his need . This process is done throughout an ontology of filters displayed to the user a network.",
                    technologies:"JavaScript, Node.js, Html, CSS",link:""},
                    {title:"LogViewer",path:'/logViewer.jpg',technologies:"Bash script, Linux, Rsyslog, JavaScript , Node.js, MySql ",description:"LogViewer is a software that aims to display the logs of all the client machines connected to the server machine through Rsysylog protocol . This software allows to the administrator to view all the logs in real time in a platform that allows him to search , filter … . The Software has two sides : the client side that aims to connect the client to the server and the server side that aims to set up the server to start receining logs and displaying them on the platform that is launched automatically after the set up.",link:""},
                    {title:"Delivry website",path:'/delivry-website.png',description:"this is an e-commerce website that aims to manage the commands of a delivery man clients could choose the store as well as the products they wanted to buy from it and the delivery man could view the commands and update their status through the admin space of the website",technologies:"Php, MySql,Apache",link:""}
                ],
                [
                    {title:"User Management Interface",path:'/userInterface.PNG',description:"This is a small university project to apply Java concepts learned in the university such as Object oriented programming , exceptions , System design and architecture , JVM internals - Java Build tools (maven, Gradle) , Unit testing (JUnit),Building dynamic web projects using Java JEE ",technologies:"Java ,PostgreSql , Hibernate",link:""},
                    {title:"Envipeace Junior",technologies:"React Native, JavaScript, Node.js, Firebase, Expo , Android Studio",path:'/envipeace.PNG',description:"ENVIPEACE-JUNIOR  is a cross platform mobile app that aims to sensitize children towards environment through an interactive educational content such as quizzs videos …"},
                    {title:"Report Generator",path:'/report.png',description:"this project was done under the context of a summer internship the goal was to understand the different operations that an employee was doing through a spreadsheet to make a software that will do the same work to generate the daily work saving him 20 min per day",technologies:"Python,Pyqt5 ,Fbs"}
                    
                ]
            ]
        }
    }
    
}
</script>

<template>
<div class="projectContainer">
   
    
    <div class="titleProject">{{title}}</div>
    <div class="descriptionProject">{{description}}</div>
    <div class="projects" >
        <div class="projectGroup" v-for="group in projects">
        <projectContainer  v-for="project in group" :image="project.path" :title="project.title" @click="()=>{show=true}"/>
        <VueModelProject v-if="show"  @click="()=>{show=false}" :project-name="project.title" :description="project.description" :technologies="project.technologies" :project-link="project.link"/> 
        </div>
    </div>
    <div class="update">
        {{textUpdate}}        
    </div>
    

    <a class="linkGit" href="">
                {{callToGit}}
     </a>
</div>
</template>
<style>
.projects{
    width: 100%;
    margin-top: 3%;
    margin-bottom: 3%;
    height: auto;
}
.projectGroup{
    width: 100%;
    height:30%;
    display:flex;
    flex-direction: row;
    justify-content: center;
    margin-top: 3%
    ;
    

}
.projectContainer{
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color:#D9D9D9 ;

}
.titleProject{
    color:#202020 ;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: x-large;
    font-weight: bold;
    margin-top: 3%;

}
.descriptionProject{
    color: #202020;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: x-large;
    font-style: italic;
    font-weight: lighter;
    margin-top: 2%;


}
.linkGit{
    padding-top: 2%;
    width: 60%;
  
    margin-bottom: 2%;
    color: #202020;
    text-align: center;
    font-size: x-large;
    font-style: italic;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #D9D9D9;


}
.update{
    width: 60%;
    margin-top: 5%;
    margin-bottom: 2%;
    color: #202020;
    text-align: center;
    font-size: x-large;
    font-style: italic;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #D9D9D9;
}
</style>
