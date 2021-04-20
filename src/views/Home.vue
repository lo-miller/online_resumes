<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <p>{{student.firstName}} {{student.lastName}}</p>
  </div>
</template>

<style>
#home {
  font-family: center;
}
</style>
<script>
export default {
  data: function () {
    return {
      message: "Welcome to Vue.js!",
      student: {
        firstName: "Stevie",
        lastName: "Wonder",
      },
    };
  },
  created: function () {},
  methods: {
    // resumeIndex: function () {
    //   console.log("resume index");
    //   // resume web request
    //   axios.get("/api/resume").then((response) => {
    //     console.log(response.data);
    //     this.resume = response.data;
    //   });
  },
};
</script>