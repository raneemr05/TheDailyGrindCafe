<script setup>
import { ref } from 'vue';
const location = ref("London");

function changeLocation(){
    if(location.value === "London")
        location.value = 'New York';
    else
        location.value = 'London';
}

const greetUser = (user) => {
        alert("Welcome " + user)
}
</script>

<template>
    <div class="header">
        <h1 style="font-weight: 800;">The Daily Grind Cafe </h1>
        <slot></slot>
        <p style="font-style: oblique; font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif">Located in the heart of {{ location }} </p>
        <button class="cta" @click="changeLocation">Change Location</button>
        <button class="cta" v-on:click="greetUser('Raneem')" > Greet User</button>
    </div>

</template>

<style scoped>
.header {
    background-color: #333;
    text-align: center;
    padding: 10px 20px;
    color: white;
    display: flex;
    align-items: center;
    justify-content: space-between;
    
}

.cta {
    padding: 10px 20px;
    font-size: 1.4rem;
    margin: 5px;
    background-color:rgb(163, 3, 3);
    color: white;
    border-radius: 10px;
    border: 2px solid rgb(168, 8, 8);
    cursor: pointer;
}

.cta:hover {
    background-color:rgb(117, 21, 21) ;
}
</style>