<template>
  <div>
    <h1>Fault List</h1>
    <div>
      <!-- a v-for basically repeats the element for each item in a list -->
      <ul>
        <!-- for each fault in the faults list, render one <li> -->
        <li v-for="(f, index) in faults" v-bind:key="f">
          <span>{{ f }}</span>
          <button v-on:click="deleteFault(index)">X</button>
          <button v-on:click="editFault(index)">Edit</button>
        </li>
      </ul>
    </div>
    <h1>Add new fault</h1>
    <input type="text" placeholder="Enter new fault here" v-model="newFault" />
    <button v-on:click="addFault">Add</button>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      faults: ["Water pipe burst", "Toilet leaking", "Lights blackout"],
      newFault: "",
    };
  },
  methods: {
    addFault: function () {
      this.faults.push(this.newFault);
    },
    deleteFault: function (indexToDelete) {
      this.faults.splice(indexToDelete, 1);
    },
    editFault: function (indexToEdit) {
      let newFaultName = prompt("Please enter new fault name");
      // this.$set takes in 3 arguments
      // 1st - Which array to change
      // 2nd - the index in the array which we want to change
      // 3rd - what we want the index to change to
      this.$set(this.faults, indexToEdit, newFaultName);
    },
  },
};
</script>

<style scoped>
</style>