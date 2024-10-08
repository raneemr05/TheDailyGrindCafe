<script setup>
</script>

<template>
    <footer class="footer">
        <p> &copy; 2024 The Daily Grind Cafe - Vue</p>
        <!-- Named slots for 2 sections -->
        <slot name="social-media"></slot> 
        <slot name="contact-info"></slot>
    </footer>
</template>
<style>
.footer{
    text-align: center;
    background-color: #333;
    color:white;
    padding: 20px;
}
</style>