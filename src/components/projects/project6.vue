<script setup>
import { ref } from 'vue';

const destroyComponentProject = ref(true);
const emit = defineEmits(["emitDestroyComponentProject"])


function exit (){
emit("emitDestroyComponentProject", destroyComponentProject);
}

</script>


<template>
    <div class="mt-10">
        <div><i class="fa-solid fa-right-to-bracket cursor" @click="exit"></i></div>
        
        HelloWorld
    </div>
</template>