<template>
  <!-- <myComp /> -->
  <ChangeName />
  <div class="cart">

    <ul>
      <li v-for="item in cartItems" :key="item.id">{{ item.title }}</li>
    </ul>
    <p v-if="cartItems.length == 0">Listeniz bos</p>
  </div>

  <Product @addCart="cartItems.push($event)" :product="product" v-for="product in productList" :key="product.id" />
</template>


<script>
  import Text from './Components/Text.vue'
  import ChangeName from './Components/ChangeName.vue'
  import Product from './Components/Products.vue'

  export default {
    components:{
      myComp: Text,
      Product: Product,
      ChangeName: ChangeName
    },
    data(){
      return{
        productList: [
          {
            id: 1,
            title: "Nodejs Lesson",
            duration: "8 saat"
          },
          {
            id: 2,
            title: "Javascript Lesson",
            duration: "15 saat"
          },
          {
            id: 3,
            title: "React Lesson",
            duration: "12 saat"
          }

        ],
        cartItems: [],
      }
    }
  }
</script>


<style>

</style>
