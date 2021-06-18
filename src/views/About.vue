<template>
  <div class="about">
    <h1>This is an about page</h1>
    <button @click="showAlert">Hello world</button>
  </div>
</template>

<script>
export default {
  methods: {
    showAlert() {
      // Use sweetalert2
      this.$swal("Hello Vue world!!!");
    },
  },
};
</script>
