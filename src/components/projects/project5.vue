<script setup>
import { ref } from 'vue';

const destroyComponentProject = ref(true);
const emit = defineEmits(["emitDestroyComponentProject"])


function exit() {
    emit("emitDestroyComponentProject", destroyComponentProject);
}

</script>


<template>
    <div class="containerProject5 raleway selectNone size0-7">
        <div class="mt-10  childContainerProject5 mb-7">
            <div class="container-exit cursor " @click="exit"><i class="fa-solid fa-rotate-left cursor mr-2"></i>Retour à
                la
                liste des
                projets</div>
            <div class="flex flexColumn alignCenter">
                <h2 class="mb-3">Réalisation de sites web avec Wordpress & le thème Divi</h2>
                <div>
                    <div class="mb-3">Octobre 2021, stage d'une durée de 2 mois effectué à l'<b>association Defis</b> à
                        Lanester (Morbihan) dans le
                        cadre de la formation ENI
                        (Bac
                        +2).
                    </div>
                    <div class="mb-3">Réalisation de sites web pour les associations <b>Alesi</b> et <b>Sauvegarde56</b>.
                    </div>
                    <div>Ces 2 sites web ont été réalisés avec le CMS Wordpress et son plugin Divi (Maquettes réalisées par
                        un
                        graphiste indépendant de l'association Défis).</div>
                    <div class="flex flexColumn justifyCenter alignCenter mt-5 size0-7">
                        <div class="flex flexRow gap5">
                            <div class="flex flexColumn">
                                <a href="http://www.alesi-asso.fr/" target="_blank" rel="noopener noreferrer">
                                    <img src="../../assets/image/logo-alesi.jpg" alt="logo association Alesi"
                                        title="Association Alesi">
                                </a>
                            </div>

                            <div class="flex flexColumn">
                                <a href="http://sauvegarde56.org/" target="_blank" rel="noopener noreferrer" class="mt-3">
                                    <img src="../../assets//image/logo-sauvegarde56.svg" alt="logo Sauvegarde56"
                                        title="Sauvegarde56">
                                </a>
                            </div>
                        </div>
                        (Ci dessus, retrouvez les sites Alesi et Sauvegarde56).
                    </div>
                </div>

            </div>

        </div>
    </div>
</template>

<style scoped>
img {
    width: 11rem !important;
}

.containerProject5 {
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

.childContainerProject5 {
    width: 70vw !important;
    display: flex;
    flex-direction: column;
    line-height: 1rem;


}
</style>
