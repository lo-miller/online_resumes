<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <p>{{firstName}} {{lastName}}</p>
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function () {
    return {
      message: "Welcome to Vue.js!",
      firstName: "Stevie",
      lastName: "Wonder",
    };
  },
  created: function () {},
  methods: {},
};
</script>