<template>
  <div>
    <h1>GREETINGS (Hands On 1)</h1>
    <h2>{{ text }}</h2>
    <button v-on:click="sayHi">Say Hi</button><br />
    <button v-on:click="sayBye">Say Goodbye</button><br />
    <button v-on:click="sleep">Sleep</button><br /><br />
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      text: "Greetings",
    };
  },
  methods: {
    sayHi: function () {
      this.text = "Hello World";
    },
    sayBye: function () {
      this.text = "Goodbye World";
    },
    sleep: function () {
      this.text = "zzz...zzz...zzz";
    },
  },
};
</script>

<style scoped>
</style>