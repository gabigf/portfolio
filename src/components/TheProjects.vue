<template>
  <section class="projects">
    <header class="projects-header">
      <span class="name">portfolio</span>
      <h2>Projects</h2>
      <p>
        A collection of my recent works, check out my
        <a href="https://github.com/gabigf" target="_blank">github</a> to see my
        code.
      </p>
    </header>
    <div class="project-container">
      <article class="project" v-for="project in projectData" :key="project">
        <div class="project-top">
          <img
            :src="require(`../assets/images/${project.imageUrl}.png`)"
            class="project-img"
          />
        </div>
        <div class="project-details">
          <h3 class="project-title">{{ project.title }}</h3>
          <p class="tech-stack">{{ project.techStack }}</p>
          <p class="project-description">{{ project.description }}</p>
          <div class="project-links">
            <a
              class="link"
              :href="project.liveSite"
              target="_blank"
              v-if="project.liveSite"
              >Live Site</a
            >
            <a class="link" :href="project.github" target="_blank">Github</a>
          </div>
        </div>
      </article>
    </div>
    <span class="thin-line project-bottom"></span>
  </section>
</template>

<script>
export default {
  setup() {
    const projectData = [
      {
        id: 1,
        title: "Mint A Lisa",
        techStack: "React, Solidity, NodeJS, CSS",
        description:
          "A Mona Lisa NFT collection running on the Ethereum blockchain.",
        imageUrl: "MintALisa",
        github: "https://github.com/AbdulSaid/MintALisa",
        liveSite: null,
      },
      {
        id: 2,
        title: "Pizza N Go",
        techStack: "jQuery, NodeJS, Express, SCSS",
        description:
          "A pizza ordering and pick up app that acts as an intermediary between the client and the restaurant.",
        imageUrl: "PizzaNGo",
        github: "https://github.com/sidpatel93/Pizza-N-Go",
        liveSite: null,
      },
      {
        id: 3,
        title: "Playlister",
        techStack: "Vue, Firebase, HTML, CSS",
        description:
          "An app that allows a user to login to view, create and delete playlists.",
        imageUrl: "Playlister",
        github: "https://github.com/gabigf/playlister",
        liveSite: "https://playlister.netlify.app/",
      },
      {
        id: 4,
        title: "Live-Chat",
        techStack: "Vue, Firebase, HTML, CSS",
        description:
          "A public chatroom that can be accessed by signing up/logging in.",
        imageUrl: "LiveChat",
        github: "https://github.com/gabigf/live-chat",
        liveSite: "https://live-chat-vue.netlify.app",
      },
      {
        id: 5,
        title: "Task Manager",
        techStack: "Vue, JS, HTML, CSS",
        description:
          "A to-do list created using vueJS and json-server. The user can create, edit and delete a task. They can also view filtered lists based on task completion.",
        imageUrl: "Task-manager",
        github: "https://github.com/gabigf/project-planner",
        liveSite: null,
      },
      {
        id: 6,
        title: "Wi-Know",
        techStack: "jQuery, HTML, SCSS",
        description:
          "A flash card app to learn about 5 different wine regions.",
        imageUrl: "Wi-Know",
        github: "https://github.com/gabigf/Wi-know2.0",
        liveSite: "https://gabigf.github.io/Wi-know2.0/index.html",
      },
    ];

    return { projectData };
  },
};
</script>

<style>
.projects {
  padding: 3rem 2rem 0 2rem;
  height: fit-content;
  margin-bottom: 8rem;
  background-image: linear-gradient(180deg, #fdf0e9 37%, transparent 37%);
  color: var(--primary);
  display: flex;
  flex-direction: column;
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
  background: #fdfaf8;
  display: flex;
  flex-direction: column;
  padding: 1rem 1rem 0 1rem;
}

.project-title {
  font-size: 1rem;
  padding-bottom: 0.25rem;
}

.tech-stack {
  font-size: 0.85rem;
  font-weight: 500;
  padding-bottom: 0.5rem;
}

.project-description {
  font-size: 0.75rem;
  color: var(--primary-light);
  height: 25px;
}

.project-links {
  padding-top: 1rem;
  align-self: flex-end;
  font-size: 0.85rem;
  font-weight: 500;
}

.project-links .link:first-of-type {
  padding-right: 1rem;
}

.link:hover {
  text-decoration: underline;
}

.project-bottom {
  margin-top: 8rem;
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
