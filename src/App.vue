<template>
  <TheNavbar />
  <Landing />
</template>

<script>
import TheNavbar from "./components/TheNavbar.vue"
import Landing from "./views/Landing.vue"


export default {
  name: "App",
  components: {
   TheNavbar,
   Landing
  }
};
</script>

<style>

</style>
