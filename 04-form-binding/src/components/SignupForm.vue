<template>
  <div>
    <h1>Sign Up Form (HANDS ON 4.6)</h1>
    <form>
      <div class="margin-space">
        <label>Username</label><br />
        <input type="text" v-model="username" /><br />
        <span>{{ usernameOK }}</span>
      </div>
      <div class="margin-space">
        <label>Password</label><br />
        <input type="password" v-model="password" /><br />
        <span>{{ passwordOK }}</span>
      </div>
      <div class="margin-space">
        <label>Programming Background</label><br />
        <input
          type="radio"
          v-model="programming"
          value="experienced"
          name="experienced"
        />Experienced
        <input
          type="radio"
          v-model="programming"
          value="intermediate"
          name="intermediate"
        />Intermediate
        <input
          type="radio"
          v-model="programming"
          value="no-nxperience"
          name="no-nxperience"
        />No Experience
      </div>
      <div class="margin-space">
        <label>Interested Programming Language</label><br />
        <input
          type="checkbox"
          v-model="langinterest"
          value="javascript"
          name="javascript"
        />Javascript
        <input
          type="checkbox"
          v-model="langinterest"
          value="java"
          name="java"
        />Java
        <input
          type="checkbox"
          v-model="langinterest"
          value="python"
          name="python"
        />Python
        <input
          type="checkbox"
          v-model="langinterest"
          value="cplus"
          name="cplus"
        />C++
      </div>
      <div class="margin-space">
        <label>Preferred Timing</label><br />
        <select v-model="timing">
          <option value="none">-----</option>
          <option value="morning">Morning</option>
          <option value="afternoon">Afternoon</option>
          <option value="evening">Evening</option>
        </select>
      </div>
      <div class="margin-space">
        <button type="submit">Submit</button>
      </div>
    </form>
    <div>
      <h1>Submitted Details</h1>
      <ul>
        <li>Username: {{ username }}</li>
        <li>Password: {{ password }}</li>
        <li>Programming Background: {{ programming }}</li>
        <li>Language Interest: {{ langinterest }}</li>
        <li>Preferred Timing: {{ timing }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      username: "",
      password: "",
      programming: "",
      langinterest: [],
      timing: "none",
    };
  },
  computed: {
    usernameOK: function () {
      if (this.username.length < 7) {
        return "Username needs to be at least 7 characters long";
      } else {
        return "";
      }
    },
    passwordOK: function () {
      let specialCharacters = "@#$%!^&";
      for (let char of this.password) {
        if (specialCharacters.includes(char)) {
          return "";
        }
      }
      return "Password must contain a symbol";
    },
  },
};
</script>

<style scoped>
.margin-space {
  margin-top: 30px;
}
</style>