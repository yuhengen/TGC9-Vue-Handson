<template>
    <div class="card product" style="width: 18rem">
      <div class="card-body">
        <h5 class="card-title">{{ product.name }}</h5>
        <div class="card-text">
          <ul>
            <li>Price: ${{ product.price }}</li>
            <li>Type: {{ product.type }}</li>
            <li>Characteristic(s): {{ product.characteristic }}</li>
          </ul>
        </div>
        <a href="#" class="btn btn-primary" @click="editTask">Edit</a>
        <a href="#" class="btn btn-danger" @click="deleteTask">Delete</a>
      </div>
    </div>
</template>

<script>
export default {
  props: ["product"],
};
</script>

<style scoped>
.product {
  margin: 5px;
}
</style>