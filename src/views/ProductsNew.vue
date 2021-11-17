<template>
  <div class="products-new">
    <form v-on:submit.prevent="createProduct()">
      
    </form>
  </div>
</template>

<style></style>

<script>
  import axios from 'axios'
  export default {
    data: function () {
      return {
        message: "Welcome to Vue.js!",
        newProductParams: {},
      };
    },
    created: function () {},
    methods: {
      createProduct: function() {
        console.log("creating product...");
        // axios
        // .post("/products", this.newProductParams)
        // .then((response) => {
        //   console.log(response.data);
        //   this.$router = response.data;
        // })
      }
    }
  };
</script>