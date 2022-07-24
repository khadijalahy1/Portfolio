<script  setup>
import projectContainer from '../utils/projectContainer.vue';
import VueModelProject from '../utils/VueModelProject.vue';

</script>

<script>
export default {

    data(){
        return{
            title:"PROJECTS",
            descriptionModel:"",
            titleModel:"",
            technologiesModel:"",
            linkModel:"",
            show:false,
            open: false,
            description:"Some of the projects I've worked on ...",
            textUpdate:"In my free time, I continue to work on personal projects and have many ideas just waiting to be realized.",
            callToGit:"To see more visit my github profile",
            projects:[
                [
                    {title:"Data4everyone",path:'/nasa.PNG',
                    description:"Data4everyone  is a project built during Nasa Space Apps Challenge Hackathon . It’s a web app that aims to guide each user through his journey of searching for data until he’ll find the one that will meet exactly his need . This process is done throughout an ontology of filters displayed to the user as a network.",
                    technologies:"JavaScript, Node.js, Html, CSS",link:"https://data4v1.herokuapp.com/"},
                    {title:"LogViewer",path:'/logViewer.jpg',technologies:"Bash script, Linux, Rsyslog, JavaScript , Node.js, MySql ",description:"LogViewer is an open source software that connects multiple clients to a server machine through Rsyslog protocol. The software helps to set up both the server and the clients to start sending and receiving logs . It also provides a platform with multiple features (search, filter ) that'll allow the server to visualize the logs of the clients in a user interface.  ",link:"https://gitlab.com/GZPERRA/rlogviewer"},
                    {title:"Delivry website",path:'/delivry-website.png',description:"It's an e-commerce website that allows the clients of a delivry man to accomplish their commands . The admin side of the website allows the delivery man to visualize and update their status .",technologies:"Php, MySql,Apache",link:"https://github.com/khadijalahy1/delivry_website"}
                ],
                [
                    {title:"User Management Interface",path:'/userInterface.PNG',description:"This is a small university project to apply Java concepts learned in the university such as Object oriented programming , exceptions , System design and architecture , JVM internals - Java Build tools (maven, Gradle) , Unit testing (JUnit),Building dynamic web projects using Java JEE ",technologies:"Java ,PostgreSql , Hibernate",link:"https://gitlab.com/khadijalahy1/users_management_interface"},
                    {title:"Envipeace Junior",technologies:"React Native, JavaScript, Node.js, Firebase, Expo , Android Studio",link:"https://github.com/khadijalahy1/ENVIPEACE_JUNIOR",path:'/envipeace.PNG',description:"ENVIPEACE-JUNIOR  is a cross platform mobile app that aims to sensitize children towards environment through an interactive educational content such as quizzs,videos …"},
                    {title:"Report Generator",link:"",path:'/report.png',description:"this project was done under the context of a summer internship the goal was to understand the different operations that an employee was doing through a spreadsheet to make a software that will do the same work to generate the daily report saving him 20 min per day.",technologies:"Python,Pyqt5 ,Fbs"}
                    
                ]
            ]
        }
    },
     methods: {
    doShow: function(title,description,technologies,link) {
      this.show=true;
      this.titleModel=title;
      this.descriptionModel=description;
      this.technologiesModel=technologies;
      this.linkModel=link;
    }
  }
    
}
</script>

<template>
<div class="projectContainer" id="projects">
    <div class="titleProject">{{title}}</div>
    <div class="descriptionProject">{{description}}</div>
    <div class="projects">
        <div class="projectGroup" v-for="group in projects">
        <projectContainer  v-for="project in group" :image="project.path" :title="project.title" @click="()=>{doShow(project.title,project.description,project.technologies,project.link)}"/>
        <VueModelProject  v-if="show==true"  :title="titleModel" :technologies="technologiesModel"  :link="linkModel"  :description="descriptionModel" @click="()=>{show=false}"/> 
        </div>
    </div>
    <div class="update">
        {{textUpdate}}        
    </div>
    <a class="linkGit" href="https://github.com/khadijalahy1">
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
.linkGit:hover{
    color: #FFD100;
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
