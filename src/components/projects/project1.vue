<script setup>
import { ref } from 'vue';

const destroyComponentProject = ref(true);
const emit = defineEmits(["emitDestroyComponentProject"])


function exit() {
    emit("emitDestroyComponentProject", destroyComponentProject);
}

</script>


<template>
    <div class="containerProject1 raleway selectNone size0-7">
        <div class="mt-10  childContainerProject1 mb-7">
            <div class="container-exit cursor " @click="exit"><i class="fa-solid fa-rotate-left cursor mr-2"></i>Retour à
                la
                liste des
                projets</div>
            <div class="flex flexColumn alignCenter">
                <h2 class="mb-3">Projet module e-learning Société Okalys <div class="ml-3 size0-7 roboto textCenter mt-1 underline"><a href="http://www.okalys.com/" target="_blank" rel="noopener noreferrer">(www.okalys.com)</a></div></h2>
                <div class="mb-3">La société Okalys, situé à Vannes (Morbihan) propose une solution de Sales Enablement
                    (Book de
                    vente
                    tactile) qui permet
                    d'optimiser
                    les rendez-vous commerciaux des forces de vente.
                    Son application repose sur la technologie <b>Progressive Web App</b>.</div>
                <div class="mb-3"> Dans le cadre du développement de l'application Okalys, j'ai eu pour mission de
                    développer dans son
                    intégralité
                    un <b>module e-learning </b>permettant d'évaluer les
                    connaissances
                    des
                    forces de vente des clients de Okalys ainsi que de participer de manière active à la gestion du projet.
                </div>
            </div>
            <div>Dans un premier temps, le module a été réalisé avec le langage Vue.js (API de composition) :
            </div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Création de composants réactifs</div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Utilisation des lifeCycles Hooks pour contrôler le
                comportement des composants </div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Transmission de données entre composants avec
                'defineProps' et 'defineEmits' </div>
            <div class="mb-3"><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Stockage des données en
                sessionStorage </div>
            <div class="mb-3"> Cette première version de ce module permet de créer et de participer à un quiz. Début 2023, j'en ai fait
                la
                démonstration à <b>Bonduelle, acteur majeur de l'agroalimentaire et client de Okalys</b>.</div>

            <div class="flex justifyCenter"><a href="https://github.com/Val56000/eLearningV2DemoClient.git" target="_blank"
                    title="E-learning GitHub Version1"><i class="fa-brands fa-github"></i></a></div>
            <div class="flex justifyCenter size0-7">Version 1 (Vue.js)</div>
        </div>

        <div class="childContainerProject1 mb-7">
            <h2 class="textCenter mb-3">Evolution du projet e-learning avec Laravel</h2>
            <div class="mb-3">Dans un second temps, la partie <b>back-end</b> a été ajouté avec
                <b> Laravel </b> :
            </div>

            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Création et migrations des tables</div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Gestions des routes</div>
            <div><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Création des controllers</div>
            <div class="mb-3"><i class="fa-solid fa-caret-down fa-rotate-270 mr-2"></i>Gestion des données avec Eloquent ORM
            </div>
            <div class="mb-3">Cela m'a permis d'ajouter de nouvelles fonctionnalités tel que la gestion des quiz, gestion
                des
                utilisateurs et la consultation des scores (Tableaux de bords dynamiques réalisés avec la librairie <b>
                    Datatables.net</b>).</div>
            <div class="mb-3">La librairie <b>Axios</b> a permis d'executer les requêtes depuis les composants Vue.js.</div>
            <div class="mb-3">Quant aux données, elles ont été stockées en base de données <b>MySql</b> (+ interface HeidiSql).</div>
            <div><i class="fa-solid fa-check mr-2"></i>En juin 2023, le module e-learning a été
                intégré à l'application Okalys.</div>
            <div class="flex justifyCenter"><a href="https://github.com/Val56000/eLearningV2DemoClient.git" target="_blank"
                    title="e-learning GitHub Version2"><i class="fa-brands fa-github"></i></a></div>
            <div class="flex justifyCenter size0-7">Version 2 (Vue.js - Laravel)</div>

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

