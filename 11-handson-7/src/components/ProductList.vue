<template>
  <div>
    <h1>Product List</h1>
    <ul>
      <li v-for="(product, index) in products" v-bind:key="index">
        {{ product }} <button @click="deleteProduct(index)">X</button>
      </li>
    </ul>
    <h2>Add new product</h2>
    <input
      type="text"
      placeholder="New product name"
      v-model="newProductName"
    />
    <button @click="addProduct">Add</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      products: ["Handbags", "Vacuum Cleaner", "Playstation 5", "Pencil Case"],
      newProductName: "",
    };
  },
  methods: {
    addProduct: function () {
      this.products.push(this.newProductName);
    },
    deleteProduct: function (index) {
      this.products.splice(index, 1);
    },
  },
};
</script>

<style scoped>
</style>