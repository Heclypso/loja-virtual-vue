<template>
    <div class="product">
        <div class="image-wrapper">
            <img class="product__image" src="https://placehold.co/120x120" alt="">
            <div class="protuct__image__tag">Novo</div>
        </div>
        <div class="product__container">
            <h2 class="product__title">Nome do produto por extenso</h2>
            <span class="product__price">R$ 157,86</span>
            <div class="product__counter">- 1 +</div>
            <span class="product__available">3 Disponíveis</span>
        </div>
    </div>
</template>

<style scoped>
.product {
    height: 186px;
    display: flex;
    border-bottom: 2px solid #FAFAFA;
    padding: 32px;
}

.image-wrapper {
    position: relative;
    width: 120px;
    height: 120px;
    margin-right: 24px;
}

.product__image {
    width: 120px;
}

.protuct__image__tag {
    position: absolute;
    top: 0;
    right: 0;
    font-size: 16px;
    line-height: 19px;
    font-style: italic;
    font-weight: 700;
    color: #fff;
    text-align: center;
    background-color: red;
    width: 80px;
    height: 40px;
    transform: rotateZ(37deg);
}

.product__container {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.product__title {
    font-size: 28px;
    font-style: italic;
    font-weight: 300;
    line-height: 28px;
    color: #000;
}

.product__price {
    width: 104px;
    background-color: #363636;
    font-size: 20px;
    color: #fff;
    padding: 4px;
}

.product__counter {
    width: 104px;
    height: 24px;
    text-align: center;
    background-color: #363636;
    font-size: 20px;
    color: #fff;
}

.product__available {
    margin-top: -4px;
    font-size: 14px;
    color: #828282;
}
</style>