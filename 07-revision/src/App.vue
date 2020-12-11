<template>
  <div id="app">
    <ImageFrame
      imageSource="https://www.humanesociety.org/sites/default/files/styles/1240x698/public/2018/08/kitten-440379.jpg?h=c8d00152&itok=1fdekAh2"
      borderColor="red"
    />
    <LoginForm v-on:user_login="processLogin" />
  </div>
</template>

<script>
import LoginForm from "./components/LoginForm";
import ImageFrame from "./components/ImageFrame";

export default {
  name: "App",
  components: {
    LoginForm,
    ImageFrame,
  },
  methods: {
    processLogin: function (user) {
      alert(user.username + " has logged in");
    },
  },
};
</script>

<style>
#app {
  margin: 50px;
}
</style>
