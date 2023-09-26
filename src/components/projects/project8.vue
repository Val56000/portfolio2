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
                <h2 class="mb-3">Quiz avec interaction multijoueurs <div
                        class="ml-3 size1 roboto textCenter mt-1 underline"><a href="https://valentinharnay-dev.fr/GWF/"
                            target="_blank" rel="noopener noreferrer">(Accéder à l'application)</a></div>
                </h2>
                <div class="mb-3">Cette application de quiz permet aux joueurs de créer leurs propres questions et d'évaluer
                    par eux mêmes les réponses des autres joueurs.</div>

            </div>
            <div>Le jeu a été réalisé sur la période de septembre 2023 avec le langage <b>Vue.js (API de composition)</b> et
                avec <b>PHP</b> côté serveur :
            </div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Mise en place du cahier des charges / Prototypage</div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Création de composants réactifs</div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Utilisation des lifeCycles Hooks pour contrôler le
                comportement des composants </div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Utilisation de Vuex (State management) pour gérer l'état global de l'application </div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Utilisation de Vuetify (Framework de composants
                UI) </div>
            <div class="mb-3"><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Stockage des données dans des
                fichiers <b>JSON </b></div>
            <div> Cette première version de cette application a été testée et approuvée par les utilisateurs.</div>

            <div class="flex flexRow justifyCenter gap3">
                <div class="flex flexColumn justifyCenter alignCenter">
                    <div><a href="https://github.com/Val56000/gamewithfriendsfront-main.git" target="_blank"
                            title="GameWithFriends Front-end GitHub Version1"><i class="fa-brands fa-github pt-5"></i></a></div>
                    <div class="flex justifyCenter size1">Front-end</div>
                </div>
                <div>
                    <div class="flex justifyCenter"><a href="https://github.com/Val56000/gamewithfriendsback-main.git"
                            target="_blank" title="GameWithFriends Back-end GitHub Version1"><i class="fa-brands fa-github pt-5"></i></a>
                    </div>
                    <div class="flex justifyCenter size1">Back-end</div>
                </div>
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
