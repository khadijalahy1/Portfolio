<script setup>
import emailjs from 'emailjs-com';
</script>
<script>
export default {
    data() {
        return {
            name: '',
            email: '',
            subject: '',
            message: ''
        }
    },
    methods: {
        sendEmail() {
            emailjs.sendForm("service_w9j2bub", "template_zsnkzpm",this.$refs.form,'kc-EnMl44sh2B-Coh',{
                name:this.name,
                email:this.email,
                message:this.message,
                subject:this.subject
            });
            this.name="";
            this.email="";
            this.subject="";
            this.message=""       
         

    }
}
}
</script>

<template>
    <div class="containerC" id="contact">
        <div style="text-align:center ; margin-top: 5%; margin-bottom: 5%;">
            <h2 style="color:#FFD100 ; margin-bottom: 2%; ">Contact Me</h2>
            <p>I am excited to hear about potential career opportunities, so I would be pleased to chat about internship
                openings in the software engineering sphere</p>
        </div>
        <div class="row">
            <div class="columnC">
                <img src="/contact.jpeg" style="width:100% ; margin-bottom: 5%;">
                <p style="color:#FFD100 ;">Email : <a href="Khadijalahy1@gmail.com"
                        style="color:#D9D9D9">Khadijalahy1@gmail.com</a> </p>
                <p style="color:#FFD100 ;">Linkedin: <a href="https://www.linkedin.com/in/khadija-al-ahyane"
                        style="color:#D9D9D9">/in/khadija-al-ahyane/</a> </p>
            </div>
            <div class="columnC">
                <form  ref="form" @submit.prevent="sendEmail">
                    <label for="name">Name</label>
                    <input type="text" id="name" v-model="name" name="name" placeholder="Your name..">
                    <label for="lname">Email</label>
                    <input type="text" id="email" v-model="email" name="email" placeholder="Your Email..">
                    <label for="lname">Subject</label>
                    <input type="text" id="subject" v-model="subject" name="subject"
                        placeholder="The subject of the discussion ">

                    <label for="subject">Message</label>
                    <textarea id="subject" name="message" v-model="message" placeholder="Write something.."
                        style="height:170px"></textarea>
                    <input type="submit" value="Submit" >
                </form>
            </div>
        </div>
    </div>


</template>
<style>
* {
    box-sizing: border-box;
}

/* Style inputs */
input[type=text],
select,
textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccc;
    margin-top: 6px;
    margin-bottom: 16px;
    resize: vertical;
    background-color: #D9D9D9;
}

input[type=submit] {
    background-color: #FFD100;
    color: #202020;
    padding: 12px 20px;
    border: none;
    cursor: pointer;
}

input[type=submit]:hover {
    background-color: #45a049;
}

/* Style the container/contact section */
.containerC {

    background-color: #202020;
    padding: 10px;
    width: 100%;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    color: #D9D9D9;
    padding-bottom: 5%;
}

/* Create two columns that float next to eachother */
.columnC {
    float: left;
    width: 50%;
    margin-top: 6px;
    padding: 20px;
}

/* Clear floats after the columns */
.row:after {
    content: "";
    display: table;
    clear: both;
}

/* Responsive layout - when the screen is less than 600px wide, make the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {

    .column,
    input[type=submit] {
        width: 100%;
        margin-top: 0;
    }
}
</style>