<script setup>
import { ref } from 'vue';
const location = ref("London");

function changeLocation(){
    if(location.value === "London")
        location.value = 'New York';
    else
        location.value = 'London';
}


</script>

<template>
    <div class="header">
        <h1> The Daily Grind Cafe located in the heart of {{ location }} </h1>
        <button class="cta" @click="changeLocation">Change Location</button>
    </div>

</template>

<style scoped>
.header {
    background-color: #333;
    text-align: center;
    padding: 10px 0px;
    color: white;
}

.cta {
    padding: 20px;
    font-size: 1.4rem;
    margin: 5px;
    background-color: rgb(48, 9, 9);
    color: white;
    border-radius: 20px;
    border: 2px solid rgb(53, 1, 1);
}

.cta:hover {
    border: 4px solid rgb(53, 1, 1);
}
</style>