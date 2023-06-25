<script setup>
import { ref } from 'vue';
import project1 from './projects/project1.vue'
import project3 from './projects/project3.vue'
import project4 from './projects/project4.vue'
import project5 from './projects/project5.vue'

const path = ref(null);

function showProject(project) {
  path.value = project;
}

function displayParentProject(destroyComponentProject) {
  if (destroyComponentProject.value == true) {
    path.value = null;
  }
}
</script>

<template>
  <div v-if="path == null" class="flex flexRow justifyCenter roboto mt-8 flexWrap gap3">
    <div class="backGroundColor1 height2 containerProject width15 radius cursor" @click="showProject('project1')">
      <div class="flex flexColumn">
        <div>
          <i class="fa-solid fa-folder-open pr-1 mb-3"></i> Module e-learning - Société Okalys (2022 -
          2023)
        </div>
        <div class="flex gap1 justifyCenter">
          <i class="fa-brands fa-vuejs"></i>
          <i class="fa-brands fa-laravel"></i>

        </div>
      </div>
    </div>
    <a class="backGroundColor1 height2 containerProject width15 radius cursor"
      href="https://github.com/Val56000/portfolio2.git" target="_blank">
      <div>
        <div class="flex flexColumn">
          <div>
            <i class="fa-solid fa-folder-open pr-1 mb-3"></i> Portfolio (2023)
          </div>
          <div class="textCenter">
            <i class="fa-brands fa-vuejs"></i>
          </div>
        </div>
      </div>
    </a>

    <div class="backGroundColor1 height2 containerProject width15 radius cursor" @click="showProject('project3')">
      <div class="flex flexColumn">
        <div>
          <i class="fa-solid fa-folder-open pr-1 mb-3"></i> Mini réseau social - Projet personnel (2022)
        </div>
        <div class="flex gap1 justifyCenter">
          <i class="fa-brands fa-js"></i>
          <i class="fa-brands fa-php"></i>
          <i class="fa-brands fa-sass"></i>
        </div>
      </div>
    </div>
    <div class="backGroundColor1 height2 containerProject width15 radius cursor" @click="showProject('project4')">
      <div class="flex flexColumn">
        <div>
          <i class="fa-solid fa-folder-open pr-1 mb-3"></i> Projet soutenance (2022)
        </div>
        <div class="flex gap1 justifyCenter">
          <i class="fa-brands fa-js"></i>
          <i class="fa-brands fa-php"></i>
        </div>
      </div>
    </div>
    <div class="backGroundColor1 height2 containerProject width15 radius cursor" @click="showProject('project5')">
      <div class="flex flexColumn">
        <div>
          <i class="fa-solid fa-folder-open pr-1 mb-3"></i> Réalisation de site web (Stage 2021)
        </div>
        <div class="flex gap1 justifyCenter">
          <i class="fa-brands fa-wordpress"></i>
        </div>
      </div>
    </div>
    <a class="backGroundColor1 height2 containerProject width15 radius cursor"
      href="https://github.com/Dagn3/ENIProjet.git" target="_blank">
      <div>
        <div class="flex flexColumn">
          <div>
            <i class="fa-solid fa-folder-open pr-1 mb-3"></i> Appli d'organisation de sorties scolaires (ENI - 2021)
          </div>
          <div class="flex gap1 justifyCenter">
            <i class="fa-brands fa-symfony"></i>
          </div>
        </div>
      </div>
    </a>
    <a class="backGroundColor1 height2 containerProject width15 radius cursor"
      href="https://github.com/ENI-groupe-2/ProjetENI.git" target="_blank">
      <div class>
        <div class="flex flexColumn">
          <div>
            <i class="fa-solid fa-folder-open pr-1 mb-3"></i>
            Appli de ventes aux enchères (ENI - 2021)
          </div>
          <div class="flex gap1 justifyCenter">
            <i class="fa-brands fa-java"></i>
          </div>
        </div>
      </div>
    </a>
  </div>
  <project1 v-if="path == 'project1'" @emitDestroyComponentProject="displayParentProject" />
  <project3 v-if="path == 'project3'" @emitDestroyComponentProject="displayParentProject" />
  <project4 v-if="path == 'project4'" @emitDestroyComponentProject="displayParentProject" />
  <project5 v-if="path == 'project5'" @emitDestroyComponentProject="displayParentProject" />
</template>

<style scoped>
.width15 {
  width: 30rem;
}

.containerProject:last-child {
  margin-bottom: 3rem;
}

.containerProject {
  box-shadow: #c0b8b8 5px 5px 8px;
  transition-duration: 0.5s;
}

.containerProject:hover,
.containerProject:focus {
  box-shadow: none;
  transition-duration: 0.5s;
}

a.containerProject {
  color: black;
}
</style>