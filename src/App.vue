<template>
  <TheNavbar />
  <Home />
</template>

<script>
import TheNavbar from "./components/TheNavbar.vue"
import Home from "./views/Home.vue"


export default {
  name: "App",
  components: {
   TheNavbar,
   Home
  }
};
</script>

<style>

</style>
