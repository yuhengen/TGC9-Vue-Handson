<template>
  <div class="counter" v-on:click="reset">
    {{ this.number }}
  </div>
</template>

<script>
export default {
  props: ["number"],
  methods: {
    reset: function () {
      this.$emit("resetNum");
    },
  },
};
</script>

<style scoped>
.counter {
  width: 250px;
  height: 250px;
  text-align: center;
  border: 1px black solid;
}
</style>