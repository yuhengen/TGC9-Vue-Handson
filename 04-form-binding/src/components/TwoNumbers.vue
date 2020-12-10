<template>
  <div>
    <h1>Sum of Two Numbers (HANDS ON 4.5)</h1>
    <div class="margin-space">
      <label>Number 1</label><br />
      <input type="number" v-model="number1" />
    </div>
    <div class="margin-space">
      <label>Number 2</label><br />
      <input type="number" v-model="number2" />
    </div>
    <br /><button v-on:click="sumOfNumber">Sum Up</button><br />
    <div class="margin-space totalbox">
      <label>SUM:</label><br /><br />
      <span class="centralize">{{ sum }}</span>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      number1: "",
      number2: "",
      sum: "NULL",
    };
  },
  methods: {
    sumOfNumber: function () {
      this.sum = parseInt(this.number1) + parseInt(this.number2);
    },
  },
};
</script>

<style scoped>
.margin-space {
  margin-top: 30px;
}
.totalbox {
  height: 100px;
  width: 100px;
  border: 1px black solid;
  text-align:center;
}
.centralize {
    margin: auto;
}
</style>