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
        <div class="container-exit cursor roboto" @click="exit"><i class="fa-solid fa-rotate-left cursor mr-2"></i>Retour à la
            liste des
            projets</div>
        <div class="flex flexColumn alignCenter">
Mini réseau social
        </div>
    </div>
</template>

