<script setup>
import "./assets/main.css"
import "./assets/bulma.min.css"
import { ref, onMounted } from 'vue';
import Home from "./components/home.vue"
import Projects from "./components/projects.vue"
import Curriculum from "./components/curriculum.vue"
import Contact from "./components/contact.vue"

const path = ref('home');
const activeMenuHamburger = ref(false);

function changeScreen(item) {
  path.value = item;
}

function toggleMenuHamburger() {

  if (activeMenuHamburger.value == false) {
    activeMenuHamburger.value = true;
    console.log('test');
    return;
  } else if (activeMenuHamburger.value == true) {
    activeMenuHamburger.value = false;
    return;
  }
}



</script>

<template>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link
    href="https://fonts.googleapis.com/css2?family=Caveat:wght@600&family=Mulish:ital,wght@0,200;1,200&family=Raleway:wght@200;400&family=Roboto&display=swap"
    rel="stylesheet">
  <nav class="roboto selectNone">
    <div class="flex alignCenter gap5 white">
      <div class="white cursor" @click="changeScreen('home')" :class="{ underline: path == 'home' }">
        Home
      </div>

      <div class="white cursor" @click="changeScreen('projects')" :class="{ underline: path == 'projects' }">
        Projects
      </div>

      <div class="white cursor" @click="changeScreen('curriculum')" :class="{ underline: path == 'curriculum' }">
        CV
      </div>

      <div class="white cursor" @click="changeScreen('contact')" :class="{ underline: path == 'contact' }">
        Contact
      </div>
    </div>
  </nav>
  <div class="menuHamburger roboto" v-if="activeMenuHamburger == true">
    <div class="cursor" @click="changeScreen('home')" :class="{ underline: path == 'home' }">Home</div>
    <div class="cursor" @click="changeScreen('projects')" :class="{ underline: path == 'projects' }">Projects</div>
    <div class="cursor" @click="changeScreen('curriculum')" :class="{ underline: path == 'curriculum' }">CV</div>
    <div class="cursor" @click="changeScreen('contact')" :class="{ underline: path == 'contact' }">Contact</div>
  </div>
  <div class="name-portfolio selectNone">
    <div>Portfolio</div>
    <div>Harnay Valentin</div>
  </div>
  <div id="menuToggle" >
    <input id="checkbox" type="checkbox">
    <label class="toggle" for="checkbox" @click="toggleMenuHamburger">
      <div class="bar bar--top"></div>
      <div class="bar bar--middle"></div>
      <div class="bar bar--bottom"></div>
    </label>
  </div>


  <Home v-if="path == 'home'" />
  <Projects v-if="path == 'projects'" />
  <Curriculum v-if="path == 'curriculum'" />
  <Contact v-if="path == 'contact'" />
</template>

<style scoped>
#menuToggle {
  position: fixed;
  top: 1.5rem;
  right: 1rem;
  display: none;
}

#checkbox {
  display: none;
}

.toggle {
  position: relative;
  width: 30px;
  cursor: pointer;
  margin: auto;
  display: block;
  height: calc(4px * 3 + 11px * 2);
}

.bar {
  position: absolute;
  left: 0;
  right: 0;
  height: 4px;
  border-radius: calc(4px / 2);
  background: #ffffff;
  color: inherit;
  opacity: 1;
  transition: none 0.35s cubic-bezier(.5, -0.35, .35, 1.5) 0s;
}

/***** Tornado Animation *****/

.bar--top {
  bottom: calc(50% + 11px + 4px/ 2);
  transition-property: bottom, transform;
  transition-delay: calc(0s + 0.35s) * .6;
}

.bar--middle {
  top: calc(50% - 4px/ 2);
  transition-property: opacity, transform;
  transition-delay: calc(0s + 0.35s * .3);
}

.bar--bottom {
  top: calc(50% + 11px + 4px/ 2);
  transition-property: top, transform;
  transition-delay: 0s;
}

#checkbox:checked+.toggle .bar--top {
  transform: rotate(-135deg);
  transition-delay: 0s;
  bottom: calc(50% - 4px/ 2);
}

#checkbox:checked+.toggle .bar--middle {
  opacity: 0;
  transform: rotate(-135deg);
  transition-delay: calc(0s + 0.35s * .3);
}

#checkbox:checked+.toggle .bar--bottom {
  top: calc(50% - 4px/ 2);
  transform: rotate(-225deg);
  transition-delay: calc(0s + 0.35s * .6);
}
</style>
