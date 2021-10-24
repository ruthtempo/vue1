<template>
    <div>
        <button @click="$emit('previousSentence')">Previous</button>
        <button @click="$emit('nextSentence')">Next</button>
    </div>
</template>
<script>
export default {
    name:'Button',
    emits:['previousSentence', 
    'nextSentence']
    
}
</script>
<style scoped>

button{
    width:25%;
    margin-left:10px;
    height:50px;
    background-color:orchid;
    cursor:pointer;
    font-size:20px;
    color:white;
    border-color: orchid;
    border-style:solid;
}

</style>