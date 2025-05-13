<template>
    <nav class="nav">
        <div class="nav__container">
        <img src="../assets/supermarket-logo.svg" alt="Logo do supermercado" class="nav__logo">
            <img src="../assets/shopping-cart-icon.svg" alt="Ícone do carrinho de compras" class="nav__icon">
        </div>
    </nav>
</template>

<style scoped>
.nav {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 74px;
    background-color: #fff;
    border-bottom: 1px solid #D5D5D5;
    padding: 8px 0px;
}

.nav__container {
    width: 90vw;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.nav__logo {
    height: 57px;
}

.nav__icon {
    width: 38px;
    height: 38px;
}
</style>