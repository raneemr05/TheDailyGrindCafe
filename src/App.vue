<!-- For logic / JS - Using composition API -->
<script setup>
// importing components using import
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import SpecialOffer from './components/SpecialOffer.vue';
import Menu from './components/Menu.vue';
import OrderForm from './components/OrderForm.vue';
</script>

<!-- For html and structure of page -->
<template>
  <div id="app">
    <Header></Header>
    <Menu></Menu>
    <OrderForm></OrderForm>
    <SpecialOffer></SpecialOffer>
    <Footer></Footer>
  </div>
</template>

<!-- For styling the page - Optional -->
<style>
</style>