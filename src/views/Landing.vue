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

  <section class="about">
    <article class="about-summary">
    <h2 class="about-header">About Me</h2>
      <p class="about-content">I have been working in the specialty coffee industry for the past 7 years. I fell into it when I joined the team at a doughnut cafe.<br><br>
      Very quickly I was promoted to be the manager, during my time there I made many changes to increase efficiency and started organizing events to increase revenue as well as implementing other small revenue channels.
      From then on I have managed 3 other cafes with small teams of around 5 people to my previous job where I managed roughly 20-25 people.</p>
    </article>
  <span class="thin-line"></span>
    <!-- <section class="faq">
      This is the FAQ
    </section> -->
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

.about {
  padding-top: 4rem;
  height: 100vh;
  background: #FDF0E9;
  color: var(--primary);
  display: flex;
  flex-direction: column;
}

.about-summary {
  display: flex;
  justify-content: space-between;
  margin: 0 2rem;
}

.thin-line{
    content: '';
    margin: 4rem 0 0 1rem;
    height: 2px;
    background-color: #F3D1BF;
    width: 80%;
    align-self: center;
  } 

.about-header {
  font-size: 3rem;
}

.about-content {
  width: 71%;
  color: var(--primary-light);
  font-size: 1.25rem;
  line-height: 32px;
}

</style>