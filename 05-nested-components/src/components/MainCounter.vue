<template>
  <div class="flex">
    <div>
      <div>
        <CounterDisplay v-bind:number="number1" v-on:resetNum="resetNum1" />
      </div>
      <div>
        <button v-on:click="increment1">+</button>
        <button v-on:click="decrement1">-</button>
      </div>
    </div>
    <div>
      <div>
        <CounterDisplay v-bind:number="number2" v-on:resetNum="resetNum2" />
      </div>
      <div>
        <button v-on:click="increment2">+</button
        ><button v-on:click="decrement2">-</button>
      </div>
    </div>
  </div>
</template>

<script>
import CounterDisplay from "./CounterDisplay";

export default {
  components: {
    CounterDisplay,
  },
  data: function () {
    return {
      number1: 123,
      number2: 321,
    };
  },
  methods: {
    increment1: function () {
      this.number1 += 1;
    },
    decrement1: function () {
      this.number1 -= 1;
    },
    increment2: function () {
      this.number2 += 1;
    },
    decrement2: function () {
      this.number2 -= 1;
    },
    resetNum1: function () {
      this.number1 = 0;
    },
    resetNum2: function () {
      this.number2 = 1;
    },
  },
};
</script>

<style scoped>
div {
  margin: auto;
  text-align: center;
}
.flex {
  display: flex;
  justify-content: space-around;
}
</style>