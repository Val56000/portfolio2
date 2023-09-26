<script setup>
import { ref } from 'vue';

const destroyComponentProject = ref(true);
const emit = defineEmits(["emitDestroyComponentProject"])


function exit() {
    emit("emitDestroyComponentProject", destroyComponentProject);
}

</script>


<template>
    <div class="containerProject1 raleway selectNone size1">
        <div class="mt-10  childContainerProject1 mb-7">
            <div class="container-exit cursor " @click="exit"><i class="fa-solid fa-rotate-left cursor mr-2"></i>Retour à
                la
                liste des
                projets</div>
            <div class="flex flexColumn alignCenter">
                <h2 class="mb-3">Projet soutenance - ENI Ecole Informatique Bac +2
                </h2>
                <div class="mb-3">Ce projet a été réalisé dans le cadre de la soutenance pour le titre de 'Développeur Web &
                    Web Mobile'.</div>

            </div>
            <div>Ce site web récapitule l'ensemble des projets réalisés au cours du stage au sein de l'association
                <b>Défis</b> à Lanester (Morbihan).
            </div>
            <div class="pt-2">Quel est le contenu de ce site ?</div>
            <div class="pt-2"><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Système d'inscription et de connexion
            </div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Présentation des projets WordPress (Divi)
            </div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Présentation du projet Python permettant de merger
                des fichiers</div>

            <div class="pt-3"> Ce projet de site web a été présenté lors de l'examen final.</div>
            <div class="flex flexColumn justifyCenter alignCenter">
                <div><a href="https://github.com/Val56000/Projet-soutenance-bac-2.git" target="_blank"
                        title="Projet soutenance GitHub"><i class="fa-brands fa-github pt-5"></i></a>
                </div>
                <div class="flex justifyCenter size1">Projet soutenance</div>
            </div>

        </div>
    </div>
</template>

<style scoped>
.fa-brands.fa-github {
    color: black !important;
}

.containerProject1 {
    width: 100vw;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

.childContainerProject1 {
    width: 70vw !important;
    display: flex;
    flex-direction: column;
    line-height: 1rem;


}
</style>