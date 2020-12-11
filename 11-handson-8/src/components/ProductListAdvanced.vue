<template>
  <div class="container">
    <h1>Products</h1>
    <input type="text" v-model="searchBy" />
    <h2>Total Cost: {{ totalCost }}</h2>
    <div class="d-flex flex-wrap">
      <Product
        v-for="p in filteredProduct"
        v-bind:product="p"
        v-bind:key="p.id"
      />
    </div>
  </div>
</template>

<script>
import Product from "./Product";

export default {
  components: { Product },
  data: function () {
    return {
      searchBy: "",
      product: [
        {
          id: 1,
          name: "Playstation 5",
          price: 500,
          type: "physical",
          characteristic: ["fragile", "limited"],
        },
        {
          id: 2,
          name: "ACME Chainsaw",
          price: 200,
          type: "physical",
          characteristic: ["hazard", "huge"],
        },
        {
          id: 3,
          name: "E-book on getting rich",
          price: 20,
          type: "digital",
          characteristic: ["limited edition", "small"],
        },
      ],
    };
  },
  computed: {
    filteredProduct: function () {
      let filtered = this.product.filter((eachProduct) => {
        return eachProduct.name
          .toLowerCase()
          .includes(this.searchBy.toLowerCase());
      });
      return filtered;
    },
    totalCost: function () {
      let reducer = (costSoFar, currentProduct) => {
        return costSoFar + currentProduct.price;
      };
      let totalCost = this.filteredProduct.reduce(reducer, 0);
      return totalCost
    },
  },
};
</script>

<style scoped>
</style>