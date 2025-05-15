<script setup>
  import Navbar from './components/Navbar.vue';
  import Product from './components/Product.vue';
  import { reactive } from 'vue';

  const estado = reactive({
    filtro: ''
  })

  let valorMedio
  let valorDosItens
  let itens
  let itensArray 

  const intervalo = setInterval(() => {
    itens = document.querySelectorAll('.product');
    const quantidadeDeItens = itens.length;
    
    if (itens.length > 0) {
      clearInterval(intervalo);

      itensArray = [...itens] ;

      itens.forEach((item) => {
        valorDosItens = parseFloat((item.children[1].children[1].innerText).split(' ')[1].split(',')[0] + '.' + (item.children[1].children[1].innerText).split(' ')[1].split(',')[1])
      });
    
      valorMedio = valorDosItens / quantidadeDeItens
    }
  }, 100);

  function getAllItens() {
    console.log(itens)
  }
  
  function getMoreExpensiveItens() {
    const itensAcimaDaMedia = itensArray.filter((item) => {
      const valorEmTexto = (item.children[1].children[1].innerText).split(' ')[1].split(',')[0] + '.' + (item.children[1].children[1].innerText).split(' ')[1].split(',')[1]
      const valor = parseFloat(valorEmTexto)

      return valor > valorMedio;
    });
    console.log(itensAcimaDaMedia)
  }

  function getCheaperItens() {
    const itensAbaixoDaMedia = itensArray.filter((item) => {
      const valorEmTexto = (item.children[1].children[1].innerText).split(' ')[1].split(',')[0] + '.' + (item.children[1].children[1].innerText).split(' ')[1].split(',')[1]
      const valor = parseFloat(valorEmTexto)

      return valor < valorMedio;
    });

    console.log(itensAbaixoDaMedia)
  }

  function getBestSellersItens() {
    console.log("Itens mais vendidos")
  }

  function getBestRatedItens() {
    console.log("Itens mais bem avaliados")
  }

  let { filtro } = estado;

  function alteraFiltro(evento) {
    filtro = evento.target.value
    
    switch(filtro) {
      case 'more-expensive':
        return getMoreExpensiveItens()

      case 'cheaper':
        return getCheaperItens()

      case 'best-sellers':
        return getBestSellersItens()

      case 'best-rated':
        return getBestRatedItens()

      default: 
        return getAllItens()
    }
  }

</script>

<template>
  <Navbar />
  <div class="container">
    <h1 class="container__title">Sessão de Itens</h1>
    <div class="container__filter">
        <button @click="alteraFiltro" value="all-products" class="container__filter__button active">Todos os Produtos</button>
        <button @click="alteraFiltro" value="more-expensive" class="container__filter__button">Mais caros</button>
        <button @click="alteraFiltro" value="cheaper" class="container__filter__button">Mais baratos</button>
        <button @click="alteraFiltro" value="best-sellers" class="container__filter__button">Mais vendidos</button>
        <button @click="alteraFiltro" value="best-rated" class="container__filter__button">Melhor avaliado</button>
    </div>
    <Product class="product" />
    <Product class="product" />
    <Product class="product" />
    <Product class="product" />
    <Product class="product" />
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
