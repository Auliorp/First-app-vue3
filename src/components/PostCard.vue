<template>
<div class="post-card">
    <h3>Tilulo</h3>
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Recusandae culpa maxime alias quasi eum! Sunt quo saepe ullam! Doloribus, accusantium atque reiciendis dolorum minima corrupti. Deleniti sit esse nam officia.</p>
    <PostButton/>
</div>
</template>

<script lang="ts" setup>
import PostButton from './PostButton.vue';
</script>

<style scoped>
.post-card{
    border-radius: 15px;
    padding: 10px;
    margin: 5px;
    border: 1px solid #ccc;
}
</style>