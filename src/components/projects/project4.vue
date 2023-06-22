<script setup>
import { ref } from 'vue';

const destroyComponentProject = ref(true);
const emit = defineEmits(["emitDestroyComponentProject"])


function exit() {
    emit("emitDestroyComponentProject", destroyComponentProject);
}

</script>


<template>
    <div class="mt-10">
        <div class="container-exit cursor roboto" @click="exit"><i class="fa-solid fa-rotate-left cursor mr-2"></i>Retour à la liste des
            projets</div>
        <div class="flex flexColumn alignCenter">
            <div>
                Stage réalisé à l'association Defis à Lanester (Morbihan)
            </div>
            <div>
                Durée du stage : 2 mois (Octobre à Décembre 2021)
            </div>
            <div>
            </div>
        </div>
    </div>
</template>

