<template>
  <div>
    <h1>DICE (Hands On 2.2 + 3.2)</h1>
    <h2 v-bind:style="{ color: diceColor }">{{ number }}</h2>
    <button v-on:click="diceNumber">Roll Dice</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      number: 0,
      diceColor: "black",
    };
  },
  methods: {
    diceNumber: function () {
      let ranNumber = Math.floor(Math.random() * 6) + 1;
      if (ranNumber % 2 == 0) {
        this.number = ranNumber + "!";
      } else {
        this.number = ranNumber;
      }
      if (ranNumber == 1) {
        this.diceColor = "red";
      } else if (ranNumber == 6) {
        this.diceColor = "green";
      } else {
        this.diceColor = "black";
      }
    },
  },
};
</script>

<style scoped>
</style>