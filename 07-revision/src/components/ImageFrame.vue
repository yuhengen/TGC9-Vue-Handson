<template>
  <div class="image">
    <img
      v-bind:src="imageSource"
      class="image-size"
      v-bind:style="{
        borderColor: borderColor,
      }"
    />
  </div>
</template>

<script>
export default {
  props: ["imageSource", "borderColor"],
};
</script>

<style scoped>
.image-size {
  height: 20vh;
  border: 1px black solid;
}
</style>