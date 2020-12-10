<template>
  <div>
    <h1>Form Practice</h1>
    <form>
      <div class="margin-space">
        <label>First Name: </label><br />
        <input type="text" v-model="first_name" />
      </div>
      <div class="margin-space">
        <label>Last Name: </label><br />
        <input type="text" v-model="last_name" />
      </div>
      <div class="margin-space">
        <input type="radio" value="male" v-model="gender" />Male
        <input type="radio" value="female" v-model="gender" />Female
      </div>
      <div class="margin-space">
        <label>Occupation:</label><br />
        <input type="radio" value="student" v-model="occupation" />Student
        <input type="radio" value="full-time" v-model="occupation" />Full-Time
        <input type="radio" value="part-time" v-model="occupation" />Part-Time
      </div>
      <div class="margin-space">
        <label>Leisure:</label><br />
        <input type="checkbox" value="sports" v-model="leisure" />Sports
        <input type="checkbox" value="reading" v-model="leisure" />Reading
        <input type="checkbox" value="sleeping" v-model="leisure" />Sleeping
        <input type="checkbox" value="eating" v-model="leisure" />Eating
        <input type="checkbox" value="hang-out" v-model="leisure" />Hang-Out
        with Friends
      </div>
      <div class="margin-space">
        <label>How did you hear about us?</label><br />
        <select v-model="hearAbout">
          <option value="none">------</option>
          <option value="friends">From Friends</option>
          <option value="facebook">From Facebook</option>
          <option value="email">From Email</option>
        </select>
      </div>
      <div class="margin-space">
        <label>Country:</label><br />
        <select v-model="country">
          <option value="sg">Singapore</option>
          <option value="my">Malaysia</option>
          <option value="th">Thailand</option>
          <option value="id">Indonesia</option>
        </select>
      </div>
    </form>
    <div>
      <h1>Your details</h1>
      <ul>
        <li>First Name: {{ first_name }}</li>
        <li>Last Name: {{ last_name }}</li>
        <li>Gender: {{ gender }}</li>
        <li>Occupation: {{ occupation }}</li>
        <li>Leisure: {{ leisure }}</li>
        <li>Hear about us from: {{ hearAbout }}</li>
        <li>Country: {{ country }}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      first_name: "",
      last_name: "",
      gender: "",
      occupation: "",
      leisure: [],
      hearAbout: "none",
      country: "sg",
    };
  },
};
</script>

<style scoped>
.margin-space {
  margin-top: 30px;
}
</style>