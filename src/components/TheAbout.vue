<template>
  <section class="about">
    <article class="about-summary">
      <header class="about-header">
        <p class="name">about</p>
        <h2 class="about-heading">Summary</h2>
      </header>
      <p class="about-content">Ability to put themselves in the merchant's shoes. It is meant to partner on the long run, and work as an extension of the merchant's team.<br><br>
      A digital agency is a business you hire to outsource your digital marketing efforts, instead of handling in-house. They can provide your business with a variety of digital solutions to promote your product or service online and help you.</p>
    </article>
    <span class="thin-line"></span>

    <div class="about-bottom">
      <section class="faq">
        <aside class="faq-header">
          <p class="name">FAQ</p>
          <p class="faq-heading">Frequently Asked Questions</p>
          <p class="faq-summary">A digital agency is a business you hire to outsource your digital marketing efforts, instead of handling in-house.</p>
          <p class="faq-btn">Contact Me</p>
        </aside>
        <FaqAccordion />
      </section>
      <span class="thin-line bottom"></span>
    </div>
  </section>
</template>

<script>
import FaqAccordion from "./FaqAccordion.vue"
export default {
  components: {
    FaqAccordion
  }
}
</script>

<style>
.about {
  padding-top: 4rem;
  background: #FDF0E9;
  color: var(--primary);
  display: flex;
  flex-direction: column;
  width: 100%;
}

.about-summary {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 0 2rem;
}

.thin-line {
  content: '';
  margin: 4rem 0 0 1rem;
  height: 2px;
  background-color: #F3D1BF;
  width: 80%;
  align-self: center;
}

.bottom {
  margin-top: 4rem;
}

.about-heading {
  padding-top: .5rem;
  font-size: 3rem;
}

.about-content {
  color: var(--primary-light);
  font-size: 1rem;
  line-height: 2rem;
  margin-top: 2rem;
}

.about-bottom {
  display: flex;
  flex-direction: column;
}

.faq {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 4rem 2rem;
}

.faq-header {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  height: 20rem;
}

.faq-heading {
  font-size: 40px;
  font-weight: 800;
  line-height: 48px;
  margin-top: 1rem;
  margin-bottom: 2rem;
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

@media only screen and (min-width: 768px) {
  .about-summary {
    flex-direction: row;
  }

  .about-content {
    width: 71%;
    margin-top: 0;
    font-size: 1.25rem;
  }
  
  .about-bottom {
    margin-top: 0;
  }

  .faq {
    flex-direction: row;
  }

  .faq-header {
    width: 33%;
  }

  .faq-heading {
    margin-top: 0;
    margin-bottom: 0;
  }
}
</style>
