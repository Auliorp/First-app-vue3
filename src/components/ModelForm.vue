<template>
<form action="">
    <input type="text" v-model="inputText">
    <input type="checkbox" v-model="agree"> Acepto los terminos y condiciones
    <select name="" id="" v-model="country">
        <option value="Spain"> Spain </option>
        <option value="Uk"> UK </option>
        <option value="France"> France </option>
    </select>
</form>
<h3>{{ inputText }}</h3>
</template>

//Estructura Composition API en su version actualizada *Con el setup*
<script lang="ts" setup>
    import { Ref, ref } from 'vue';

    let inputText:Ref<string> = ref("");
    let agree:Ref<boolean> = ref(true);
    let country = ref("Uk")

</script>

//Estructura Composition API en su version actualizada *Sin el setup*
<!-- <script lang="ts">

import { Ref, ref, defineComponent } from 'vue';
export default defineComponent({
    setup(){
        let inputText:Ref<string> = ref("");
            return {inputText}
    }
})
</script> -->

//Estructura Option API en su version estandar *Sin el setup*
<!-- <script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
    data(){
            return {
                inputText: "", 
            }
    }
})
</script> -->

<style scoped>
</style>