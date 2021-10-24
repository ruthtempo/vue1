<template>
    <div>
        <div v-if="!hasClicked">
            <Welcome @start="hasClicked = true"/>
        </div>
        <div v-else>
            <Button @next-sentence="clickNextSentence" @previous-sentence="clickPreviousSentence"/>
            <Escena v-bind:escenes="myLocalEscenes" v-bind:activeSentence="currentSentence" /> 
        </div>
    </div>      
</template>
<script>
import Escena from "./Escena"
import Button from "./Button"
import Welcome from "./Welcome.vue"

export default {
    name: "Home",
    components: {
        Escena,
        Button,
        Welcome,
    },
    data(){
        return{
            myLocalEscenes :[
                {text: "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial", img:""},
                {text: "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.", img:""},
                {text: "L'heroi va decidir travessar la porta que el portava a casa", img:require("../assets/1.jpg")},
                {text: "Mentrestant, altres heroes no van tenir tanta sort en la seva elecció ...", img:""},
            ],
            currentSentence : 0,
            hasClicked: false,
        }
    },
    methods:{
        clickNextSentence(){
            
            if(this.currentSentence < this.myLocalEscenes.length -1) this.currentSentence ++;
            // console.log(this.myLocalEscenes.length, this.currentSentence)
        },
        clickPreviousSentence(){
        //    this.currentSentence>0? this.currentSentence-- : this.currentSentence;

        //    this.currentSentence = Math.max(0, this.currentSentence - 1)

            if(this.currentSentence > 0) this.currentSentence--;

            // this.currentSentence = this.currentSentence > 0 ? this.currentSentence-1 : 0
        }
    }
}
</script>