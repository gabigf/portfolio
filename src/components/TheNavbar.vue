<template>
  <nav>
    <h2 class="logo">GG</h2>

    <!-- Tablets and desktop starting at 720px window width -->
    <ul class="nav-options" v-if="windowWidth >= 720">
      <li class="nav-link">Projects</li>
      <li class="nav-link">About</li>
      <li class="nav-link">Resume</li>
    </ul>
    <button class="secondary-dark contact" v-if="windowWidth >= 720">
      Contact
    </button>

    <!-- Mobile starting a 719px -->
    <label class="menu" v-else>
      <input type="checkbox" checked />
      <div>
        <span></span>
        <span></span>
      </div>
    </label>
  </nav>
</template>

<script>
import { useWindowSize } from "vue-window-size";

export default {
  setup() {
    const { width, height } = useWindowSize();
    return {
      windowWidth: width,
      windowHeight: height,
    };
  },
};
</script>

<style>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 90%;
  margin: 1rem auto;
  background: transparent;
}

.logo {
  cursor: pointer;
  font-size: 3rem;
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


/* Credit to Aaron Iker for the code on his codepen */
.menu {
  display: flex;
  --icon: white;
  align-self: center;
  perspective: 600px;
  width: 48px;
  height: 48px;
  position: relative;
  cursor: pointer;
  -webkit-tap-highlight-color: transparent;
  align-items: center;
  justify-content: center;
}

.menu input {
  display: none;
}

.menu input + div span {
  --rotateY: 0deg;
  --background: transparent;
  transform: rotateY(var(--rotateY));
  transform-style: preserve-3d;
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  border-radius: 6px;
  border: 1px solid rgba(255, 255, 255, 0.295743);
  background: var(--background);
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  transition: transform 0.6s cubic-bezier(0.2, 0.64, 0.48, 1.24);
}

.menu input + div span:before,
.menu input + div span:after {
  --rotate: 0deg;
  content: "";
  position: absolute;
  width: 16px;
  height: 2px;
  border-radius: 1px;
  top: 50%;
  left: 50%;
  background: var(--icon);
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  transform: translate(-50%, -50%) rotate(var(--rotate)) translateZ(6px);
}

.menu input + div span:first-child {
  --background: var(--secondary);
}

.menu input + div span:first-child:before {
  --rotate: -45deg;
}

.menu input + div span:first-child:after {
  --rotate: 45deg;
}

.menu input + div span:last-child {
  --rotateY: 180deg;
}

.menu input + div span:last-child:before {
  box-shadow: 0 -5px 0 var(--icon), 0 5px 0 var(--icon);
}

.menu input + div span:last-child:after {
  display: none;
}

.menu input:checked + div span:first-child {
  --rotateY: -180deg;
}

.menu input:checked + div span:last-child {
  --rotateY: 0deg;
}

</style>
