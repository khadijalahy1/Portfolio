<script setup>
</script>
<script>
export default {
    props:{
        description:{
            type:String,
            required:true
        },
        title:{
            type:String,
            required:true
        },
        technologies:{
            type:String,
            required:true
        },
        link:{
            type:String,
            required: true
        }
    },
    data(){
        return{
            descItems:[
                {title:"Description :",content:this.description},
                {title:"Technologies :",content:this.technologies},
                {title:"Link to Project :",content:this.link}
            ]
        
        }
    }

}


</script>

<template>
<div class="pop-up">
    <img src="/close.png" class="closeBtn" alt="" @click="()=>{show=!show}">
    <div class="descTitle">{{title}}</div>
    <div class="descItems">
        <div class="descItem" v-for="item in descItems" >

            <div class="itemTitle" v-if="item.content!=''">{{item.title}}</div>
            <div class="itemContent"  v-if="item.content!='' && item.title!='Link to Project :'">{{item.content}}</div>
            <div class="itemContent"  v-else-if="item.content!='' && item.title=='Link to Project :'"><a :href="item.content">{{item.content}}</a></div>


        </div>        
    </div>
</div>
</template>
<style scoped>

.pop-up{
    position: fixed;
    top: 15vh;
    left: 20%;
    right: 20%;
    bottom: 15vh;
    width: 60%;
    height: auto;
    background-color: #fff4b2;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;


}
.descItems{
    width:80% ;
    height:70vh;
    display:flex;
    flex-direction: column    
}
.descItem{
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
    color: #1c0f0f;
    font-size: large;
    margin-top: 2%;
    
}
.itemTitle{
    font-weight: bold;
    width: 60%;

}
.itemContent{
    font-weight: lighter;
    font-size: medium;
    margin-top: 2%;
}

.descTitle{
    margin-top: 5%;
    width: 60%;
    height: 10vh;
    color:#1c0f0f;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: x-large;
    text-align: center;

}
.closeBtn{
    position:absolute;
    top: 5%;
    right: 3%;

}


</style>