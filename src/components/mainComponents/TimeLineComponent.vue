<script setup>
import ExperienceContainer from '../utils/ExperienceContainer.vue';
import ImageSmallContainer from '../utils/ImageSmallContainer.vue';


</script>
<script>
export default {
    data() {
        return {
            title: "Timeline",
            description: "A little bit about me ...",
            experiences: [
                { id: 0, date: "2018-2020", location: "Reda Slaoui", description: "Mathematic and physic track", image: "cpge.jpg" },
                { id: 1, date: "2020-2023", location: "AIAC", description: "Computer science engineering student", image: "aiac.jpg" },
                { id: 2, date: "Summer 2021", location: "Petrom", description: "Software engineer intern", image: "petrom.png" },
                { id: 3, date: "November 2021 - April 2022", location: "Manara", description: "Bootcamp", image: "manara.jpg" },
                { id: 4, date: "Present", location: "", description: "Working on ongoing projects ", image: "github.jpg" },

            ]


        }
    }
}

</script>
<template>
    <div class="parentTL" id="timeline">
        <div class="titleTL">{{ title }}</div>
        <div class="descriptionTL">{{ description }}</div>
        <div class="itemsTL">
            <div v-for="experience of experiences" class="itemTL">
                <div class="expLeftContainer">
                    <ExperienceContainer v-if="experience.id % 2 == 0" :date="experience.date"
                        :location="experience.location" :description="experience.description" />

                </div>


                <div class="imagexp">
                    <ImageSmallContainer :path="experience.image" />

                </div>
                <div class="expRightContainer">
                    <ExperienceContainer v-if="experience.id % 2 != 0" :date="experience.date"
                        :location="experience.location" :description="experience.description" />

                </div>




            </div>
        </div>


        <div class="line">
        </div>

    </div>

</template>
<style>
.expLeftContainer {
    width: 45%;
    display: flex;
    flex-direction: row;
    justify-content: end;
}

.expRightContainer {
    width: 40%
}

.imagexp {
    z-index: 2;
    height: auto;

    left: 50%;


}

.itemsTL {
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;


}

.itemTL {
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: row;
    margin-bottom: 5%;
}

.titleTL {
    width: 100%;
    height: auto;
    background-color: #202020;
    z-index: 2;
    padding-top: 5%;
    text-align: center;
    padding-bottom: 2%;
    font-weight: bold;

}

.descriptionTL {
    width: 100%;
    height: auto;
    background-color: #202020;
    z-index: 2;
    padding-top: 1%;
    text-align: center;
    padding-bottom: 5%;

}

.parentTL {

    background-color: #202020;
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    color: #D9D9D9;
    font-size: x-large;


}

.line {
    position: absolute;
    background-color: #D9D9D9;
    width: 5px;
    height: 200vh;
    left: 50%;
    z-index: 1;
}
</style>