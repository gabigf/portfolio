<template>
  <TheHome />
  <TheAbout />
  <TheProjects />
  <TheResume />
</template>

<script>
import TheHome from "../components/TheHome.vue"
import TheAbout from "../components/TheAbout.vue"
import TheProjects from "../components/TheProjects.vue"
import TheResume from "../components/TheResume.vue"

export default {
components: {
   TheHome,
   TheAbout,
   TheProjects,
   TheResume
  }
}
</script>

<style>

</style>
