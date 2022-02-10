<template>
  <nav>
    <h2 class="logo">Gabi</h2>

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

  .logo {
    cursor: pointer;
  }

  .logo:hover {
    color: var(--secondary);
  }

  .nav-options {
    display: flex;
    justify-content: space-between;
    width: 30%;
    color: white;
  }

  .nav-link {
    cursor: pointer;
    border-bottom: 2px solid transparent;
  }

  .nav-link:hover {
    border-bottom: 2px solid rgba(255, 255, 255, 0.64);
  }

  .contact {
    text-transform: uppercase;
    font-weight: 800;
    margin-top: 0.5rem;
  }

</style>
