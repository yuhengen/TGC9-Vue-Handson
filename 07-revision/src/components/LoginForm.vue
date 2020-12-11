<template>
  <div id="app">
    <h1>Vue Revision</h1>
    <!-- binding is connecting an attribute or props to a data variable -->
    <!-- Whenever the template sees a variable, it will search in 4 places:
    1. Data
    2. Props
    3. Methods
    4. Computed -->

    <!-- binding to a placeholder in template -->
    <p>{{ instructions }}</p>

    <!-- bind to attribute or props -->
    <!-- v-model is two-way binding -->
    <div>
      <input type="text" placeholder="username" v-model="username" />
    </div>
    <div>
      <input type="text" placeholder="password" v-model="password" />
    </div>
    <button v-on:click="loginPressed">Login</button>
  </div>
</template>

<script>
export default {
  // data is private content aka variables of the component. Cannot be accessed by others
  data: function () {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    loginPressed: function () {
      this.$emit("user_login", {
        username: this.username,
        password: this.password,
      });
    },
  },
};
</script>

<style scoped>
</style>
