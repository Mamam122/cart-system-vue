<template>
    <div> 
        <h1>Your Cart</h1>

        <CartItemCard 
            v-for="product in product " 
            :key="product.id"
            :product="product"/>

        <CartSumarryPaymentCard 
            />
    </div>
</template>

<script>
import CartItemCard from '../components/cart/ItemCard.vue'
import CartSumarryPaymentCard from '../components/cart/SummaryPaymentCard.vue'

export default {
    components:{
        CartItemCard,
        CartSumarryPaymentCard
    },
    computed: {
        product(){
            return this.$store.getters.cartItem
        }
    }
}
</script>