<template>
<form action="">
    <input type="text" v-model="inputText">
    <h3>{{ inputText }}</h3>
</form>
</template>

//Estructura Composition API en su version actualizada *Con el setup*
<!-- <script lang="ts" setup>
import { Ref, ref } from 'vue';

let inputText:Ref<string> = ref("");

</script> -->

//Estructura Composition API en su version actualizada *Sin el setup*
<script lang="ts">

import { Ref, ref, defineComponent } from 'vue';
export default defineComponent({
    setup(){
        let inputText:Ref<string> = ref("");
            return {inputText}
    }
})


</script>

<style scoped>
</style>