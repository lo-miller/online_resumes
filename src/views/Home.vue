<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <div v-for="student in students">
     <p> {{student.first_name}} {{student.last_name}} </p>
      </div>
  </div>
</template>

<style>
#home {
  font-family: center;
}
</style>
<script>
import axios from "axios";
export default {
  data: function () {
    return {
      message: "Welcome to Vue.js!",
      students: [],
    };
  },
  created: function () {
    this.resumeIndex();
  },
  methods: {
    resumeIndex: function () {
      console.log("resume index");
      // resume web request
      axios.get("/api/students").then((response) => {
        console.log(response.data);
        this.students = response.data;
      });
    },
  },
};
</script>