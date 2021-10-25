<template>
    <div>
        <ul>
            <li :class="{selected : index == activeSentence}" v-for="(e, index) in escenes" :key="index" >{{e.text}}</li>
        </ul>
    </div>
</template>
<script>
export default {
    name:"Escena",
    props:{
        escenes:Array,
        activeSentence:Number,
    },
    // props: ['escenes'],
    data(){
        return{
            escena:"El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial"
        }
    }
}
</script>
<style scoped>

    li{
        border:1px solid palegoldenrod;
        background-color: whitesmoke;
        border-radius:55px;
        padding:15px;
        margin:25px;
        list-style: none;
        opacity:0.95;
    }

    .selected{
        background-color: powderblue;
        border-color:powderblue;
        
    }
</style>