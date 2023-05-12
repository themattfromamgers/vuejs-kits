<template>

    <div class="product">
        <strong>eğitim:  {{ product.title }}</strong>
        <p>saat: {{ product.duration }}  </p>
    </div>
    <p>{{ message }}</p>
    <button @click="addToCart(product)">Ekle</button>
</template>


<script>
export default {
    props: ['product'],
    methods: {
        addToCart(product){
            this.$emit('addCart', product)
        }
    }
}
</script>
<style>
.product{
    border: 2px dashed #cc1010;
    padding: 10px;
    width: 250px;
}
</style>