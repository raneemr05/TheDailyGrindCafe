<!-- Conditional Rendering directives - v-if, v-else -->
<!-- v-html -->
<script setup>
const isDiscountAvailable = false;
const htmlContent = '<u> Freshly brewed coffee, just for you! </u>'
</script>
<template>
    <div class="special">
        <h3>Special Offer</h3>
        <!-- Using v-html directive -->
        <p v-html="htmlContent"></p>
        <p v-if="isDiscountAvailable">Enjoy 20% Discount on all orders! </p>
        <p v-else>Enjoy 10% discount only for memebers</p>
    </div>
</template>

<style scoped>
.special{
    text-align: center;
    padding: 20px;
    background-color: bisque;
    color:brown;
}
</style>