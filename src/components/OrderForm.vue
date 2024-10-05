<script setup>
import { reactive, ref } from 'vue';

// Creates a reactive form object
const orderForm = reactive({
    name: '',
    coffee: '',
    milk: '',
    sugar: false
});

//Function to handle the form submission
const submitOrder = () =>{
    formSubmitted.value = true;
    console.log('Order Submitted: ', orderForm);
}

// Boolean to check if the formSubmitted
const formSubmitted = ref(false);

</script>

<template>
    <div class="container">
        <h2> Order Your Coffee Now </h2>
        <form @submit.prevent="submitOrder">
            <!-- Name Input -->
            <label for="name">Your Name:</label>
            <input type="text" v-model="orderForm.name" id="name" placeholder="Enter your name">
            <!-- Dropdown (Coffee Selection)-->
             <label for="coffee"> Choose Your Coffee: </label>
             <select id="coffee" v-model="orderForm.coffee">
                <option value=""> </option>
                <option>Cappuccino</option>
                <option>Latte</option>
                <option>Espresso</option>
             </select>

             <!-- Milk Preference (Radio Buttons)-->
              <label for="milk"> Milk Preference: </label>
              <label>
              <input type="radio" v-model="orderForm.milk" value="Whole Milk"> Whole Milk
              </label>
              <label>
              <input type="radio" v-model="orderForm.milk" value="Skim Milk"> Skim Milk
            </label>
            <label>
              <input type="radio" v-model="orderForm.milk" value="Almond Milk"> Almond Milk
            </label>

              <!-- Extras: (Checkbox) -->
               <label for="extras"> Extras: </label>
               <label>
               <input type="checkbox" v-model="orderForm.sugar"> Extra Sugar
            </label>

               <!-- Submit button -->
               <button type="submit">Order Now</button>
        </form>

        <!-- Order Summary to be visible after the form is submitted -->
        <div class="order-summary" v-if="formSubmitted">
            <h3> Order Summary </h3>
            <p>Name: {{ orderForm.name }} </p>
            <p>Coffe Type: {{ orderForm.coffee }} </p>
            <p>Milk Preference: {{ orderForm.milk }} </p>
            <p>Extra Sugar: {{ orderForm.sugar ? 'Yes' : 'No' }} </p>
        </div>
    </div>

</template>

<style scoped>
.container{
    padding: 20px;
    text-align: center;
    color:white;
}

form{
    display: flex;
    flex-direction: column;
    max-width: 400px;
    margin: 0 auto;
}

input, select, button{
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button{
    background-color: rgb(152, 5, 5);
    color: white;
    cursor: pointer;
    border:none;
    font-size:1.2em;
}

label, p{
    margin: 10px 0 5px;
}

.order-summary{
    margin-top: 20px;
    padding: 15px;
    text-align: center;
}
</style>