<template>
  <section class="resume">
    <header class="resume-header">
      <span class="name">resume</span>
      <h2 class="resume-heading">Professional Review</h2>
    </header>

    <div class="resume-container">
      <section class="resume-left">
        <div class="work-experience resume-component">
          <p class="title-line"></p>
          <h3 class="resume-title">Work Experience</h3>
          <article>
            <p class="category-title">
              Crew Cafe & Collective - Barista Manager
            </p>
            <p class="category-details">Dec 2018 - Jun 2020</p>
          </article>
          <article>
            <p class="category-title">
              Saint-Henri Micro-Torréfacteur - Wholesale Representative
            </p>
            <p class="category-details">Jan 2018 - Dec 2020</p>
          </article>
        </div>

        <div class="tech-skills resume-component">
          <p class="title-line"></p>
          <h3 class="resume-title">Technical Skills</h3>
          <div class="category-details-container">
            <div class="left-skills">
              <p>Javascript</p>
              <p>VueJS</p>
              <p>ReactJS</p>
              <p>jQuery</p>
              <p>HTML</p>
              <p>CSS</p>
              <p>SASS/SCSS</p>
              <p>Firebase</p>
            </div>
            <div class="right-skills">
              <p>Ruby on Rails</p>
              <p>SQL</p>
              <p>PostgreSQL</p>
              <p>PHP</p>
              <p>MongoDB</p>
              <p>Express</p>
              <p>NodeJS</p>
              <p>Mocha</p>
            </div>
          </div>
        </div>

        <div class="tools resume-component">
          <p class="title-line"></p>
          <h3 class="resume-title">Tools</h3>
          <div class="category-details-container">
            <div class="left-skills">
              <p>Git</p>
              <p>Github</p>
              <p>CLI</p>
              <p>npm</p>
            </div>
            <div class="right-skills">
              <p>Figma</p>
              <p>Bootstrap</p>
              <p>Storybook</p>
              <p>Cypress</p>
            </div>
          </div>
        </div>

        <div class="langs resume-component">
          <p class="title-line"></p>
          <h3 class="resume-title">Languages</h3>
          <p>English</p>
          <p>French</p>
          <p>Portuguese</p>
        </div>
      </section>

      <section class="resume-right">
        <div class="education resume-component">
          <p class="title-line"></p>
          <h3 class="resume-title">Education</h3>
          <article>
            <p class="category-title">Lighthouse Labs</p>
            <p class="category-details">Oct 2021 - Jan 2021</p>
            <p>Full Stack Web Development Bootcamp</p>
          </article>
          <article>
            <p class="category-title">Lighthouse Labs</p>
            <p class="category-details">Oct 2021 - Jan 2021</p>
            <p>Full Stack Web Development Bootcamp</p>
          </article>
        </div>

        <div class="online-courses resume-component">
          <p class="title-line"></p>
          <h3 class="resume-title">Online Courses</h3>
          <article>
            <p class="category-title">Lighthouse Labs</p>
            <p class="category-details">Oct 2021 - Jan 2021</p>
            <p>Full Stack Web Development Bootcamp</p>
          </article>
          <article>
            <p class="category-title">Lighthouse Labs</p>
            <p class="category-details">Oct 2021 - Jan 2021</p>
            <p>Full Stack Web Development Bootcamp</p>
          </article>
          <article>
            <p class="category-title">Lighthouse Labs</p>
            <p class="category-details">Oct 2021 - Jan 2021</p>
            <p>Full Stack Web Development Bootcamp</p>
          </article>
        </div>

        <div class="Awards resume-component">
          <p class="title-line"></p>
          <h3 class="resume-title">Awards</h3>
          <article>
            <p class="category-title">SCA</p>
            <p class="category-details">Spring</p>
            <p>Full Stack Web Development Bootcamp</p>
          </article>
          <article>
            <p class="category-title">SCA</p>
            <p class="category-details">Spring</p>
            <p>Full Stack Web Development Bootcamp</p>
          </article>
        </div>
      </section>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
.resume {
  display: flex;
  flex-direction: column;
  width: 97%;
  margin: 0 2rem 0 2rem;
}

.resume-heading {
  font-size: 2.5rem;
  line-height: 48px;
  font-weight: 800;
}

.resume-container {
  display: flex;
}

.resume-left {
  margin-right: 6.5rem;
}

.resume-component {
  margin-top: 5.5rem;
  font-size: 1.25rem;
  line-height: 2rem;
}

.title-line {
  content: "";
  height: 2px;
  background-color: var(--secondary);
  width: 48px;
  margin-bottom: 1rem;
}

.resume-title {
  font-size: 2rem;
  margin-bottom: 2rem;
}

.category-title {
  font-weight: 600;
}

.category-details {
  color: var(--light-font);
}

.resume-component article:first-of-type, .resume-component article:nth-of-type(2)  {
  margin-bottom: 2rem;
}

.category-details-container {
  display: flex;
}

.left-skills {
  margin-right: 7.5rem;
  width: 114px;
}
</style>
