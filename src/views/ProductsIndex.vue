<template>
  <div class="products-index">
    <div v-for="product in products">
      <p><b>Id: </b>{{ product.id }}</p>
      <p><b>Name: </b>{{ product.name }}</p>
      <p><b>Price: </b>{{ product.price }}</p>
      <p><b>Description: </b>{{ product.description }}</p>
      <p><b>Supplier: </b>{{ product.supplier.id }}</p>
      <p><b>Images Junk: </b>{{ product.images}}
      <hr>
    </div>
  </div>
</template>

<style></style>

<script>
  import axios from 'axios';
  export default {
    data: function () {
      return {
        message: "Welcome to Vue.js!",
        products: [],
      };
    },
    created: function () {
      this.getProducts();
    },
    methods: {
      getProducts: function () {
        console.log("in getProducts...");
        axios.get("/products").then(response => {
          console.log(response.data);
          this.products = response.data;
        })
      }
    },
  };
</script>