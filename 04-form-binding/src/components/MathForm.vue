<template>
  <div>
    <h1>Computed Properties (Practice)</h1>
    <div class="margin-space">
      <label>Number 1</label><br />
      <input type="number" v-model="number1" placeholder="First Number" />
    </div>
    <div class="margin-space">
      <label>Number 2</label><br />
      <input type="number" v-model="number2" placeholder="Second Number" />
    </div>
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
      number1: 0,
      number2: 0,
    };
  },
  computed: {
    sum: function () {
      return parseInt(this.number1) + parseInt(this.number2);
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
  text-align: center;
}
.centralize {
  margin: auto;
}
</style>