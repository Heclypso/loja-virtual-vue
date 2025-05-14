<script setup lang="ts">
  import Navbar from './components/Navbar.vue';
  import Product from './components/Product.vue';
</script>

<template>
  <Navbar></Navbar>
  <div class="container">
    <h1 class="container__title">Sessão de Itens</h1>
    <div class="container__filter">
        <button class="container__filter__button active">Todos os Produtos</button>
        <button class="container__filter__button">Mais caros</button>
        <button class="container__filter__button">Mais baratos</button>
        <button class="container__filter__button">Mais vendidos</button>
        <button class="container__filter__button">Melhor avaliado</button>
    </div>
    <Product></Product>
    <Product></Product>
    <Product></Product>
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
  margin: 56px auto 0 auto;
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

.container__filter {
  height: 40px;
  background-color: #F9F9F9;
}

.container__filter__button {
  height: inherit;
  width: 20%;
  border-radius: 0px;
  border: none;
  border-right: 1px solid #dfdfdf;
  font-size: 24px;
  color: #C5C5C5;
  font-weight: 300;
  }

.active {
  background-color: #fff;
  color: #202020;
  border: none;
  border-bottom: 2px solid #202020;
  font-weight: 400;
}
</style>
