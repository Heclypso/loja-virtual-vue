<template>
    <div class="product">
        <div class="image-wrapper">
            <img class="product__image" src="../assets/nintendo-switch.png" alt="">
            <img class="protuct__image__tag" src="../assets/new-product-tag.svg" alt="Etiqueta de produto novo">
            <span class="product__price">R$ 157,86</span>
        </div>
        <div class="product__container">
            <h2 class="product__title">Nome do produto por extenso</h2>
            <div class="product__info__container">
                <span class="product__available">3 Disponíveis</span>
                <span class="product__bought">10 Comprados no ultimo mês</span>
            </div>
            <div class="product__stars__container">
                <img class="product__stars" src="../assets/star-filled.svg" alt="Estrela de avaliação vazia">
                <img class="product__stars" src="../assets/star-filled.svg" alt="Estrela de avaliação vazia">
                <img class="product__stars" src="../assets/star-filled.svg" alt="Estrela de avaliação vazia">
                <img class="product__stars" src="../assets/star-half-filled.svg" alt="Estrela de avaliação vazia">
                <img class="product__stars" src="../assets/star-empty.svg" alt="Estrela de avaliação vazia">
            </div>
            <div class="product__counter">Quantidade: 1</div>
            <div class="product__btn">Adicionar ao carrinho</div>
        </div>
    </div>
</template>

<style scoped>
.product {
    height: 214px;
    display: flex;
    border-bottom: 2px solid #FAFAFA;
    padding: 32px;
}

.image-wrapper {
    position: relative;
    width: 120px;
    height: 148px;
    margin-right: 24px;
    display: flex;
    flex-direction: column;
    background-color: #FAFAFA;
    align-items: center;

}

.product__image {
    width: 80px;
    margin: 8px;
}

.protuct__image__tag {
    position: absolute;
    top: 0;
    right: 0;
}

.product__price {
    background-color: #363636;
    font-size: 20px;
    color: #fff;
    padding: 4px 10px;
    width: 100%;
    position: relative;
}

.product__price::after {
    content: '';
    width: 9px;
    height: 32px;
    background-color: #525252;
    position: absolute;
    top: 0;
    right: 0;
}

.product__container {
    display: flex;
    flex-direction: column;
}

.product__title {
    font-size: 28px;
    font-style: italic;
    font-weight: 340;
    line-height: 28px;
    color: #000;
}

.product__info__container {
    display: flex;
    align-items: center;
    gap: 8px;
    height: 16px;
}

.product__available {
    font-size: 14px;
    color: #828282;
}

.product__bought {
    font-size: 14px;
    color: #828282;
}

.product__stars__container {
    display: flex;
}

.product__stars {
    margin-left: -2px;
}

.product__counter {
    width: 143px;
    height: 32px;
    background-color: #D6DAE2;
    font-size: 12px;
    padding: 8px;
    color: #000000;
    border-radius: 10px;
    border: .5px solid #B0B4BC;
    line-height: 15px;
    margin-top: 16px;
}

.product__btn {
    width: 143px;
    height: 32px;
    background-color: #FFEA00;
    border-radius: 16px;
    font-size: 12px;
    padding: 8px;
    margin-top: 5px;
    font-weight: 450;
}
</style>