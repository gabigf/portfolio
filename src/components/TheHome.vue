<template>
  <section class="home">
    <article class="intro">
      <h3 class="name">Gabriela Guimarães</h3>
      <p class="tag-line">Making digital products</p>
      <p class="summary">
        I provide a full service range including technical skills, design,
        business understanding.
      </p>
      <div class="contact-container">
        <button class="primary-btn">See my work</button>
        <p>Download my CV</p>
      </div>
    </article>
    <aside class="img-container">
      <img
        class="home-img"
        src="@/assets/images/home-img.png"
        alt="Home page image"
      />
    </aside>
  </section>
</template>

<script>
export default {};
</script>

<style>
.home {
  display: flex;
  flex-direction: column-reverse;
  justify-content: flex-end;
  align-items: center;
  margin-top: 1rem;
  height: 120vh;
}

.img-container {
  height: 36%;
}

.home-img {
  height: 100%;
}

.intro {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  width: 90%;
  height: 30rem;
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
  margin-top: 1rem;
}

.contact-container p {
  margin-left: 3rem;
  cursor: pointer;
  border-bottom: 2px solid transparent;
}

.contact-container p:hover {
  border-bottom: 2px solid rgba(255, 255, 255, 0.64);
}

@media only screen and (min-width: 768px) {
  .home {
    flex-direction: row;
    justify-content: space-around;
    margin-top: 5.5rem;
    height: 80vh;
  }

  .img-container {
    height: 100%;
  }

  .intro {
    width: 32rem;
    height: 24rem;
  }

  .contact-container {
    margin-top: 0;
  }
}
</style>
