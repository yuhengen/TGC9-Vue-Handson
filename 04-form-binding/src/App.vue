<template>
  <div id="app" class="flexit">
    <div><Form /></div>
    <div>
      <TwoNumbers />
    </div>
    <div>
      <SignupForm />
    </div>
    <div>
      <MathForm />
    </div>
    <div>
      <Services />
    </div>
  </div>
</template>

<script>
import Form from "./components/Form";
import TwoNumbers from "./components/TwoNumbers";
import SignupForm from "./components/SignupForm";
import MathForm from "./components/MathForm";
import Services from "./components/Services";

export default {
  name: "App",
  components: {
    Form,
    TwoNumbers,
    SignupForm,
    MathForm,
    Services,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 100px;
}
.flexit {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}
</style>
