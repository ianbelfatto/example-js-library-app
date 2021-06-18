<template>
  <div class="home">
    <h1>All Popups</h1>
    <div v-for="popup in popups" v-bind:key="popup.id">
      <p>{{ popup }}</p>
    </div>
  </div>
</template>

<style></style>

<script>
import axios from "axios";
export default {
  data: function () {
    return {
      message: "Welcome to Vue.js!",
      popups: [],
    };
  },
  created: function () {
    this.indexPopups();
  },
  methods: {
    indexPopups: function () {
      axios.get("/popups").then((response) => {
        console.log("popups index", response);
        this.popups = response.data;
      });
    },
  },
};
</script>
