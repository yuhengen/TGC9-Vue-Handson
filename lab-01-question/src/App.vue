<template>
  <div id="app">
    <SayGreetings></SayGreetings>
    <Counter></Counter>
    <Dice></Dice>
  </div>
</template>

<script>
import SayGreetings from "./components/SayGreetings";
import Counter from "./components/Counter";
import Dice from "./components/Dice";

export default {
  name: "App",
  components: {
    SayGreetings,
    Counter,
    Dice,
  },
};
</script>

<style>
#app {
  margin-left: 10vw;
}
</style>
