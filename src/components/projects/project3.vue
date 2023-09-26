<script setup>
import { ref } from 'vue';

const destroyComponentProject = ref(true);
const emit = defineEmits(["emitDestroyComponentProject"])


function exit() {
    emit("emitDestroyComponentProject", destroyComponentProject);
}

</script>


<template>
    <div class="containerProject3 raleway selectNone size1">
        <div class="mt-10  childContainerProject3 mb-7">
            <div class="container-exit cursor roboto" @click="exit"><i
                    class="fa-solid fa-rotate-left cursor mr-2"></i>Retour à la
                liste des
                projets</div>
            <div class="flex flexColumn alignCenter mb-3">
                <h2 class="mb-3">Projet personnel - mini reseau social</h2>
                <div class="mb-3">Ce projet a été réalisé dans le but de mettre en pratique les compétences acquises pendant
                    la formation ENI (bac +2).</div>
                <div class="mb-3">Ce mini réseau social a été réalisé de la façon suivante :
                    <lu>
                        <li><b>Php : </b>CRUD + sécurité</li>
                        <li><b>Javascript :</b> Manipulation du DOM + Utilisation API (OpenWeatherMap - API Météo)</li>
                        <li><b>Scss : </b>Gérer l'apparence des éléments</li>
                    </lu> <br>
                    <div>Les <b>fonctionnalités</b> de l'application :
                    <lu>
                        <li>Inscription et connexion</li>
                        <li>Modification et suppression du profil utilisateur</li>
                        <li>Consulter des données météo</li>
                        <li>Consulter des pages web</li>
                        <li>Envoyer des messages via un tchat</li>
                        <li>Jeu du 'Juste Prix intégré'</li>
                        <li>Générateur de citations intégré</li>
                    </lu>
                </div>
                </div>

            </div>
            <div class="flex justifyCenter"><a href="https://github.com/Val56000/lets-talk.git" target="_blank"
                    title="Projet réseau social - GitHub"><i class="fa-brands fa-github"></i></a></div>
            <div class="flex justifyCenter size1 mb-5">Accès GitHub</div>
            <div class="flex justifyCenter">
                <figure>
                    <video class="langages" controls>
                        <source src="../../assets/video/video1.mp4" type="video/mp4">
                        Votre navigateur ne prend pas en charge la lecture de vidéos.
                    </video>
                    <figcaption class="italic textCenter">Vidéo de démonstration</figcaption>
                </figure>
            </div>
        </div>
    </div>
</template>


<style scoped>
.fa-brands.fa-github {
    color: black !important;
}

.containerProject3 {
    width: 100vw;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

.childContainerProject3 {
    width: 70vw !important;
    display: flex;
    flex-direction: column;
    line-height: 1rem;


}
</style>

