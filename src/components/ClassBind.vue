
//otra forma de representar v-bind:class es la siguiente --> :class eliminando el "v-bind"
<template>
    <p v-bind:class="{'danger': hasError}">El mensaje se ha enviado satisfactoriamente.</p>
</template>

//Estructura Composition API en su version estandar *Sin el setup*
<!-- <script lang="ts">
import {defineComponent} from 'vue';
export default defineComponent({
    name: 'ClassBind',
    setup(){
        let hasError = true;
        return {hasError};
    }
})
</script> -->

//Estructura Composition API en su version actualizada *Con el setup*
<!-- <script lang="ts" setup>
let hasError = true;
</script> -->

//Estructura Option API en su version estandar *Sin el setup*
<script lang="ts" >
import { defineComponent } from 'vue';
export default defineComponent({
    name: 'ClassBind',
    data(){
        return {
            hasError: true
        }
    }
})
</script>

<style >
.danger{
    color: red;
}
</style>