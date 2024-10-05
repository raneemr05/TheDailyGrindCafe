<script setup>

const menuItems = [
    {id: 1, name:'Cappuccino', price: 4.5, img: 'https://images.immediate.co.uk/production/volatile/sites/30/2020/08/cappucino-32dbfba.jpg' },
    {id: 2, name: 'Espresso', price: 3.0, img: 'https://www.tasteofhome.com/wp-content/uploads/2023/03/TOH-espresso-GettyImages-1291298315-JVcrop.jpg' },
    {id: 3, name: 'Latte', price: 4.0, img: 'https://www.allrecipes.com/thmb/Wh0Qnynwdxok4oN0NZ1Lz-wl0A8=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/9428203-9d140a4ed1424824a7ddd358e6161473.jpg'}
];
console.log(menuItems);
</script>

<template>
<section class="menu">  
    <h2> Our Menu</h2>
    <p> Explore our delicious offerings</p>
    <!-- using v-for directive to display the items  -->
    <ul>
        <li v-for="item in menuItems" :key="item.id">
            <img v-bind:src="item.img" v-bind:alt="item.name" class="menu-image">
            <div class="item-description">
                <!-- Text Interpolation - to access a variable from the script and use it in template -->
                {{ item.name }} <br>  ${{ item.price }}
            </div>
        </li>
    </ul>
</section>
</template>

<style scoped>
.menu{
    padding: 20px;
    background-color: #f7f7f7;
    color: black;
}

ul{
    list-style-type: none;
    padding: 0;
    margin: 20px;
    display: flex;
    justify-content: space-evenly;
}
.menu-image{
    width: 200px;
    height: 200px;
    margin-right: 15px;
    border: 2px solid rgb(88, 4, 4);
    border-radius: 50%;
}

.item-description{
    text-align: center;
    font-size: 1.1em;;
}

.menu-image:hover{
    border: 6px solid rgb(88, 4, 4);
}
</style>