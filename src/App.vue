<script setup lang="ts">
  import Navbar from './components/Navbar.vue';
  import Product from './components/Product.vue';
</script>

<template>
  <Navbar></Navbar>
  <div class="container">
    <h1 class="container__title">Sessão de {sessão}</h1>
    <Product></Product>
    <Product></Product>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Work Sans", sans-serif;
  font-optical-sizing: auto;
  font-style: normal;
}


body {
  background-color: #E9E9E9;
}
</style>

<style scoped>
.container {
  width: 90vw;
  height: 662px;
  margin: 56px 80px;
  background-color: #fff;
}

.container__title {
  width: 100%;
  height: 64px;
  background-color: #202020;
  font-size: 36px;
  font-style: italic;
  color: #fff;
  line-height: 32px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
