<template>
  <section class="about">
    <article class="about-summary">
    <h2 class="about-header">About Me</h2>
      <p class="about-content">Ability to put themselves in the merchant's shoes. It is meant to partner on the long run, and work as an extension of the merchant's team.<br><br>
      A digital agency is a business you hire to outsource your digital marketing efforts, instead of handling in-house. They can provide your business with a variety of digital solutions to promote your product or service online and help you.</p>
    </article>
  <span class="thin-line"></span>
  </section>
</template>

<script>
export default {

}
</script>

<style>
.about {
  padding-top: 4rem;
  height: 100vh;
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
</style>
