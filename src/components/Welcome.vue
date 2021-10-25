<template>
    <div id="welcome-page">
        <h3>{{title}}</h3>
        <p>{{explanation}}</p>
        <button @click="$emit('start')">Start!</button>  
    </div>
    
</template>

<script>
export default {
    name:"Welcome",

    data() {
        return {
            title: "Welcome!",
            explanation: "This project is a demo for a future project. Click start to see what's under construction! ",
        }
    },
    emits:['start']
    
    
}
</script>

<style scoped>
#welcome-page{
    background-color: powderblue;
    padding:3rem;
    height:70vh;

}

button{
    padding:1rem;
    font-size: 20px;
    background-color: orchid;
    border-radius: 30%;;
    border-color:orchid;
    border-style:solid;
    color:white;
    cursor:pointer;
}

h3{
    font-size:50px;
    color:orchid;
}
</style>