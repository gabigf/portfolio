<template>
  <section class="about">
    <article class="about-summary">
    <h2 class="about-header">About Me</h2>
      <p class="about-content">Ability to put themselves in the merchant's shoes. It is meant to partner on the long run, and work as an extension of the merchant's team.<br><br>
      A digital agency is a business you hire to outsource your digital marketing efforts, instead of handling in-house. They can provide your business with a variety of digital solutions to promote your product or service online and help you.</p>
    </article>
    <span class="thin-line"></span>

    <section class="faq">
      <aside class="faq-header">
        <p class="name">FAQ</p>
        <p class="faq-heading">Frequently Asked Questions</p>
        <p class="faq-summary">A digital agency is a business you hire to outsource your digital marketing efforts, instead of handling in-house.</p>
        <p class="faq-btn">Contact Me</p>
      </aside>

    <FaqAccordion />
    </section>
  </section>
</template>

<script>
import FaqAccordion from "./FaqAccordion.vue"
export default {
  components: {
    FaqAccordion
  },
  setup() {

  }
}
</script>

<style>
.about {
  padding-top: 4rem;
  height: 140vh;
  background: #FDF0E9;
  color: var(--primary);
  display: flex;
  flex-direction: column;
  width: 100%;
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

.faq {
  display: flex;
  justify-content: space-between;
  margin: 1.5rem 2rem;
}

.faq-header {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 33%;
  height: 304px;
}

.faq-heading {
  font-size: 40px;
  font-weight: 800;
  line-height: 48px;
}

.faq-summary {
  line-height: 32px;
  color: var(--primary-light);
}

.faq-btn {
  background: transparent;
  color: var(--primary);
  line-height: 2rem;
  width: fit-content;
  padding: 0;
  border-bottom: 1px solid transparent;
  cursor: pointer;
}

.faq-btn:hover {
  border-bottom: 1px solid var(--primary);
  background: transparent;
}
</style>
