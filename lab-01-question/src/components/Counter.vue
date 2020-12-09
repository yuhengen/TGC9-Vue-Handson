<template>
  <div>
    <h1>COUNTER (Hands On 2.1 + 3.1)</h1>
    <h2 v-bind:style="{ color: numberColor }">{{ counter }}</h2>
    <span v-if="even == true">{{ oddEven }}</span>
    <span v-else>{{ oddEven }}</span
    ><br /><br />
    <button v-on:click="increase">+</button>
    <button v-on:click="decrease">-</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      counter: 0,
      oddEven: "Even",
      numberColor: "green",
    };
  },
  methods: {
    increase: function () {
      this.counter += 1;
      if (this.counter % 2 == 0) {
        this.oddEven = "Even";
        this.numberColor = "Green";
      } else {
        this.oddEven = "Odd";
        this.numberColor = "Red";
      }
    },
    decrease: function () {
      this.counter -= 1;
      if (this.counter % 2 == 0) {
        this.oddEven = "Even";
        this.numberColor = "Green";
      } else {
        this.oddEven = "Odd";
        this.numberColor = "Red";
      }
    },
  },
};
</script>

<style scoped>
</style>