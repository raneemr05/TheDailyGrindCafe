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
    <Header> Welcome to the cafe </Header>
    <Menu></Menu>
    <SpecialOffer> <h2> ONLY FOR YOU </h2></SpecialOffer>
    <OrderForm></OrderForm>
    <SpecialOffer></SpecialOffer>
    <Footer>
      <template v-slot:social-media>
        <p> Follow us on: </p>
          <a href="#"> Instagram</a>
          <a href="#"> Facebook</a>
      </template>
      <template v-slot:contact-info>
        <p> Contact us: info@thedailygrind.com </p>
      </template>
    </Footer>
  </div>
</template>

<!-- For styling the page - Optional -->
<style>
a{
  color:brown;
}
</style>