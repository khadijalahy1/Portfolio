<script  setup>
import skillsComponent from '../../components/utils/skillsContainer.vue'
</script>
<script>
export default {
    data(){
        return{
            skillsTitle:"SKILLS",
            description:"Some of the things I've learned",
            skills:[
                [{path:"/python.png",title:"Python",description:" Python is a language I use often and I have had significant experience with . On august 2021, I’ve used it during my summer internship and this year I’ve managed to solve over 300 problem on Leetcode using this language."},
                {path:"/cpp.png",title:"cpp",description:" I started using this language on 2022 when I started participating on competitive programming contests"},
                {path:"/java.png",title:"Java",description:"We’ve used this language in the university to learn many concepts such as Design patterns , Oriented object programming ,handling exceptions ... I practiced what we’ve learned on small side project "}],
                [{path:"/nodes.png",title:"Node.js",description:" I have used Node.js in many projects where I’ve experienced with some of its modules such as Express ."},
                {path:"/java-script.png",title:"JavaScript/Html/Css",description:" I often develop web applications using JavaScript,Html,CSS as well as Node.js and mySql for the backend"},
                {path:"/sql-server.png",title:"Sql",description:"while working on side projects I often use  relational database management system to manage its data . I’m most familiar with MySql , PostgreSql and Sql plus"}],
                [{path:"/react.png",title:"React Native",description:" I’ve used this framework to build a side project during a competition I’ve participated in . I’m also familiar with expo and React-Native Cli as those are the tools I used to build the app."}]
            ]
        }
    }

}
</script>
<template>
    <div class="skills" id="skills">
        <div class="componentTitle">{{skillsTitle}}</div>
        <div class="componentDescription">{{description}}</div>
        <div class="skillsContainer">
            <div class="skillRow" v-for="group in skills">
            <skillsComponent v-for="item in group" :title="item.title" :description="item.description" :path="item.path" />
            
            </div>
            

        </div>
        <a  id="resume" class="ResumeButton" href="https://drive.google.com/file/d/1SMhx2Ke7iRl6PxMk56-PX_s8KR6DggfE/view">
           Resume
        </a>
     
    </div>
</template>
<style>
.ResumeButton{
    width:20%;
    height:9vh;
    margin-top: 5%;
    margin-bottom: 5%;
    background-color:#FFD100;
    color: #202020;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-weight: bold;
    font-size: large;
}
.ResumeButton:hover{
    opacity: 0.7;
}
.skillsContainer{
    width: 100%;
    margin-top: 3%;
    margin-bottom: 3%;
    height: auto;
}
.skills{   
    padding-top:5%;
    background-color:#202020 ;
    display: flex;
    flex-direction: column;
    align-items: center;
    width:100%;
    height:auto;
    margin: 0%;
}
.componentTitle{
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: x-large;
    font-weight: bolder;
    color:#D6D6D6
}
.componentDescription{
    margin-top: 2%;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: large;
    font-weight: lighter;
    font-style: italic;
    color:#D6D6D6

}
.skillRow{
    width: 100%;
    height:30%;
    display:flex;
    flex-direction: row;
    justify-content: center;
    margin-top: 3%
    ;
    

}
</style>
