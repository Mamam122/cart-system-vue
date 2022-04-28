<template>
    <div class="cart-item-card">
        <h3>Cart Total : Rp{{cart_total}}</h3>
        <button class="view-product-button"> Pay by Transfer</button>
    </div>
</template>

<script>
export default {
    props:['product'],
    computed:{
        cart_total(){
            return this.$store.getters.cartTotal
        }
    }
}
</script>