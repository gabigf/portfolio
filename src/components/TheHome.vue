<template>
  <section class="home">
    <article class="intro">
      <h3 class="name">Gabriela Guimarães</h3>
      <p class="tag-line">Making digital products</p>
      <p class="summary">I provide a full service range including technical skills, design, business understanding.</p>
      <div class="contact-container">
        <button class="primary-btn">See my work</button>
        <p>Contact Me</p>
      </div>
    </article>
    <aside>
      <img class="home-img" src="@/assets/images/home-img.png" alt="Home page image">
    </aside>
  </section>
</template>

<script>
export default {

}
</script>

<style>
.home {
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin-top: 5.5rem;
  height: 80vh;
}

.intro {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  width: 32rem;
  height: 24rem;
}

.name {
  text-transform: uppercase;
  color: var(--secondary);
  line-height: 2rem;
  font-size: 1rem;
  letter-spacing: 3px;
  font-weight: 400;
}

.tag-line {
  font-size: 4.5rem;
  text-transform: capitalize;
  letter-spacing: -2px;
  font-weight: 800;
}

.summary {
  color: rgba(255, 255, 255, 0.64);
  line-height: 2rem;
}

.contact-container {
  display: flex;
  align-items: center;
}

.contact-container p {
  margin-left: 3rem;
  cursor: pointer;
  border-bottom: 2px solid transparent;
}

.contact-container p:hover {
  border-bottom: 2px solid rgba(255, 255, 255, 0.64);
}
</style>
