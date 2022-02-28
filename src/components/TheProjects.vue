<template>
  <section class="projects">
    <header class="projects-header">
      <span class="name">portfolio</span>
      <h2>Projects</h2>
      <p>A collection of my recent works, check out my <a href="https://github.com/gabigf" target="_blank">github</a> to see my code.</p>
    </header>
    <div class="project-container">
      <article class="project" v-for="project in projectData" :key="project">
        <div class="project-top">
          <img :src="require(`../assets/images/${project.imageUrl}.png`)" class="project-img" />

        </div>
        <div class="project-details">
          <h3 class="project-title">{{ project.title }}</h3>
          <p class="tech-stack">{{ project.techStack }}</p>
          <p class="project-description">{{ project.description }}</p>
          <div class="project-links">
            <a class="link" :href="project.liveSite" target="_blank" v-if="project.liveSite">Live Site</a>  
            <a class="link" :href="project.github" target="_blank">Github</a>
          </div>
        </div>
      </article>
    </div>
  </section>
</template>

<script>
export default {
  setup() {
    const projectData = [
      {
        id: 1,
        title: 'Mint A Lisa',
        techStack: 'React, Solidity, NodeJS, CSS',
        description: 'A Mona Lisa NFT collection running on the Ethereum blockchain.',
        imageUrl: 'MintALisa',
        github: 'https://github.com/AbdulSaid/MintALisa',
        liveSite: "www.gabi.pro"
      },
      {
        id: 2,
        title: 'Pizza N Go',
        techStack: 'jQuery, NodeJS, Express, SCSS',
        description: 'A pizza ordering and pick up app that acts as an intermediary between the client and the restaurant.',
        imageUrl: 'PizzaNGo',
        github: 'https://github.com/sidpatel93/Pizza-N-Go'
      },
      {
        id: 3,
        title: 'Playlister',
        techStack: 'Vue, Firebase, HTML, CSS',
        description: 'An app that allows a user to login to view, create, edit and delete playlists.',
        imageUrl: 'Playlister',
        github: 'https://github.com/gabigf/playlister',
        liveSite: "www.gabi.pro"
      },
      {
        id: 4,
        title: 'Live-Chat',
        techStack: 'Vue, Firebase, HTML, CSS',
        description: 'A pizza ordering and pick up app that acts as an intermediary between the client and the restaurant.',
        imageUrl: 'LiveChat',
        github: 'https://github.com/sidpatel93/Pizza-N-Go',
        liveSite: "www.gabi.pro"
      },
      {
        id: 5,
        title: 'Task Manager',
        techStack: 'jQuery, NodeJS, Express, SCSS',
        description: 'A pizza ordering and pick up app that acts as an intermediary between the client and the restaurant.',
        imageUrl: 'Task-manager',
        github: 'https://github.com/sidpatel93/Pizza-N-Go',
        liveSite: "www.gabi.pro"
      },
      {
        id: 6,
        title: 'Wi-Know',
        techStack: 'jQuery, NodeJS, Express, SCSS',
        description: 'A pizza ordering and pick up app that acts as an intermediary between the client and the restaurant.',
        imageUrl: 'Wi-Know',
        github: 'https://github.com/sidpatel93/Pizza-N-Go',
        liveSite: "www.gabi.pro"
      }
    ];

    return { projectData }
  }
}
</script>

<style>
.projects {
  padding: 3rem 2rem 0 2rem;
  height: 150vh;
  width: 100%;
  background-image: linear-gradient(180deg, #FDF0E9  37%, transparent 37%);
  color: var(--primary);
}

.project-container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 190%;
  padding-bottom: 2rem;
}

.project {
  border-radius: 6px;
  height: 346px;
  width: 100%;
  background: var(--light-bg);
  display: flex;
  flex-direction: column;
}

.projects-header {
  margin-bottom: 6rem;
}

.projects-header h2 {
  font-size: 2.5rem;
  padding: 1rem 0 1rem 0;
}

.projects-header p {
  color: var(--primary-light);
  line-height: 2rem;
  max-width: 470px;
}

.projects-header p a:hover {
  text-decoration: underline;
}

.project-top {
  height: 61%;
  display: flex;
  justify-content: center;
  align-items: flex-end;
}

.project-img {
  width: 300px;
  padding-bottom: 1rem;
}

.project-details {
  height: 39%;
  border-radius: 0px 0px 4.28412px 4.28412px;
  background: #FDFAF8;
  display: flex;
  flex-direction: column;
  padding: 1rem 1rem 0 1rem;
}

.project-title {
  font-size: 1rem;
  padding-bottom: .25rem;
}

.tech-stack {
  font-size: .85rem;
  font-weight: 500;
  padding-bottom: .5rem;
}

.project-description {
  font-size: .75rem;
  color: var(--primary-light);
  height: 25px;
}

.project-links {
  padding-top: 1rem;
  align-self: flex-end;
  font-size: .85rem;
  font-weight: 500;
}

.project-links .link:first-of-type {
  padding-right: 1rem;
}

.link:hover {
  text-decoration: underline;
}


@media only screen and (min-width: 768px) {
  .project-container {
    display: grid;
    grid-column-gap: 2rem;
    grid-row-gap: 2rem;
    grid-template-columns: 1fr 1fr 1fr;
    height: initial;
  }

  .projects {
    padding: 4rem 2rem 0 2rem;
  }

  .projects-header h2 {
    font-size: 3rem;
    padding: 1rem 0 1rem 0;
  }

  .project {
    height: 346px;
    width: 434px;
  }

  .project-img {
    width: 400px;
    padding-bottom: 0.5rem;
  }
}

</style>
