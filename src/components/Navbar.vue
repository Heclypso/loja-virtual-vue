<template>
    <nav class="nav">
        <img src="../assets/supermarket-logo.svg" alt="Logo do supermercado" class="nav__logo">
        <div class="nav__container">
            <img src="../assets/shopping-cart-icon.svg" alt="Ícone do carrinho de compras" class="nav__icon">
            <span class="nav__icon__counter">0</span>
        </div>
        
    </nav>
</template>

<style scoped>
.nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 74px;
    background-color: #fff;
    border-bottom: 1px solid #D5D5D5;
    padding: 8px 80px;
}

.navbar__container {
    position: relative;
}

.nav__logo {
    height: 57px;
}

.nav__icon {
    width: 38px;
    height: 38px;
    position: relative;
}

.nav__icon__counter {
    position: absolute;
    top: 0;
    right: 0;
}
</style>