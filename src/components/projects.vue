<script setup>
import { ref } from 'vue';
import project1 from './projects/project1.vue'
import project2 from './projects/project2.vue'
import project3 from './projects/project3.vue'
import project4 from './projects/project4.vue'
import project5 from './projects/project5.vue'
import project6 from './projects/project6.vue'
import project7 from './projects/project7.vue'

const path = ref(null);

function showProject(project) {
    path.value = project;
}


function displayParentProject (destroyComponentProject){
    if (destroyComponentProject.value == true) {
        path.value = null;
    }
}
</script>


<template>
    <div v-if="path == null" class="flex flexRow justifyCenter roboto mt-10 flexWrap gap5">
        <div class="backGroundColor1 height2 containerProject width15 radius cursor" @click="showProject('project1')">
            <div class="flex flexColumn">
                <div><i class="fa-solid fa-folder-open pr-1 mb-3"></i> Module eLearning - Société Okalys (2022 -
                    2023)</div>
                <div class="flex gap1 justifyCenter"><i class="fa-brands fa-laravel"></i><i class="fa-brands fa-vuejs"></i>
                </div>
            </div>
        </div>

        <div class="backGroundColor1 height2 containerProject width15 radius cursor" @click="showProject('project2')">
            <div class="flex flexColumn">
                <div><i class="fa-solid fa-folder-open pr-1 mb-3"></i> Portfolio (2023)</div>
                <div class="textCenter"><i class="fa-brands fa-vuejs"></i></div>

            </div>
        </div>

        <div class="backGroundColor1 height2 containerProject width15 radius cursor"  @click="showProject('project3')">
            <div class="flex flexColumn">
                <div><i class="fa-solid fa-folder-open pr-1 mb-3"></i> Mini réseau social (Projet personnel - 2022)</div>
                <div class="flex gap1 justifyCenter"><i class="fa-brands fa-js"></i><i class="fa-brands fa-php"></i><i
                        class="fa-brands fa-sass"></i></div>
            </div>
        </div>
        <div class="backGroundColor1 height2 containerProject width15 radius cursor" @click="showProject('project4')">
            <div class="flex flexColumn">
                <div><i class="fa-solid fa-folder-open pr-1 mb-3"></i> Projet soutenance (2022)</div>
                <div class="flex gap1 justifyCenter"><i class="fa-brands fa-js"></i><i class="fa-brands fa-php"></i>
                </div>
            </div>
        </div>
        <div class="backGroundColor1 height2 containerProject width15 radius cursor" @click="showProject('project5')">
            <div class="flex flexColumn">
                <div><i class="fa-solid fa-folder-open pr-1 mb-3"></i> Réalisation de site web (Stage 2021)</div>
                <div class="flex gap1 justifyCenter"><i class="fa-brands fa-wordpress"></i>
                </div>
            </div> 
        </div>
        <div class="backGroundColor1 height2 containerProject width15 radius cursor"  @click="showProject('project6')">
            <div class="flex flexColumn">
                <div><i class="fa-solid fa-folder-open pr-1 mb-3"></i> Appli d'organisation de sorties scolaires (ENI - 2021)
                </div>
                <div class="flex gap1 justifyCenter"><i class="fa-brands fa-symfony"></i>
                </div>
            </div> 
        </div>
        <div class="backGroundColor1 height2 containerProject width15 radius cursor" @click="showProject('project7')">
            <div class="flex flexColumn">
                <div><i class="fa-solid fa-folder-open pr-1 mb-3"></i> Appli de ventes aux enchères (ENI - 2021)

                </div>
                <div class="flex gap1 justifyCenter"><i class="fa-brands fa-java"></i>
                </div>
            </div> 
        </div>


    </div>
    <project1 v-if="path == 'project1'" @emitDestroyComponentProject="displayParentProject"/>
    <project2 v-if="path == 'project2'" @emitDestroyComponentProject="displayParentProject"/>
    <project3 v-if="path == 'project3'" @emitDestroyComponentProject="displayParentProject"/>
    <project4 v-if="path == 'project4'" @emitDestroyComponentProject="displayParentProject"/>
    <project5 v-if="path == 'project5'" @emitDestroyComponentProject="displayParentProject"/>
    <project6 v-if="path == 'project6'" @emitDestroyComponentProject="displayParentProject"/>
    <project7 v-if="path == 'project7'" @emitDestroyComponentProject="displayParentProject"/>
</template>

<style scoped>
.width15 {
    width: 30rem;
}

.containerProject:last-child {
    margin-bottom: 5rem;
}

.containerProject {
    box-shadow: #c0b8b8 5px 5px 8px;
}

.containerProject:hover, .containerProject:focus{
    box-shadow: none;
    transition-duration: 0.5s;
}
</style>