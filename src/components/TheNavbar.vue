<template>
  <nav>
    <h2 class="logo">Gabi</h2>

    <ul class="nav-options">
      <li class="nav-link">Projects</li>
      <li class="nav-link">About</li>
      <li class="nav-link">Resume</li>
      <li class="nav-link contact">Contact</li>
    </ul>
  </nav>
</template>

<script>
export default {

}
</script>

<style>
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 90%;
    margin: 0.5rem auto;
    background: transparent;
  }

  .nav-options {
    display: flex;
    justify-content: space-between;
    width: 30%;
    color: white;
  }


</style>