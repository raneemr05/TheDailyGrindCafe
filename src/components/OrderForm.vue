<script setup>
</script>

<template>
    <div class="container">
        <h2> Order Your Coffee Now </h2>
        <form>
            <!-- Name Input -->
            <label for="name">Your Name:</label>
            <input type="text" id="name" placeholder="Enter your name">

            <!-- Dropdown (Coffee Selection)-->
             <label for="coffee"> Choose Your Coffee: </label>
             <select id="coffee">
                <option value=""> </option>
                <option>Cappuccino</option>
                <option>Latte</option>
                <option>Espresso</option>
             </select>

             <!-- Milk Preference (Radio Buttons)-->
              <label for="milk"> Milk Preference: </label>
              <label>
              <input type="radio" value="Whole Milk"> Whole Milk
              </label>
              <label>
              <input type="radio" value="Skim Milk"> Skim Milk
            </label>
            <label>
              <input type="radio" value="Almond Milk"> Almond Milk
            </label>

              <!-- Extras: (Checkbox) -->
               <label for="extras"> Extras: </label>
               <label>
               <input type="checkbox"> Extra Sugar
            </label>

               <!-- Submit button -->
               <button type="submit">Order Now</button>
        </form>

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
</style>