<template>
  <nav>
    <h2 class="logo-container"><img class="logo" src="@/assets/images/logo.svg" /></h2>

    <ul class="nav-options">
      <li class="nav-link">Projects</li>
      <li class="nav-link">About</li>
      <li class="nav-link">Resume</li>
    </ul>
      <button class="secondary-dark contact">Contact</button>
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
    width: 80%;
    margin: 0.5rem auto;
    background: transparent;
  }

  .nav-options {
    display: flex;
    justify-content: space-between;
    width: 30%;
    color: white;
  }

  .contact {
    text-transform: uppercase;
    font-weight: 800;
    margin-top: 0.5rem;
  }

</style>