<template>
    <p v-bind:style="{ backgroundColor: '#ccc', color: changeColor }">El mensaje se ha enviado satisfactoriamente.</p>
    <button v-on:click="handleClick()">Cambiar color</button>
</template>

//Estructura Option API en su version estandar *Sin el setup*
<!-- <script lang="ts">
  import { defineComponent } from 'vue';
export default defineComponent({
    name:'ClassBindingStyle',
    data(){
        return {
            changeColor: '#fff'
        }
    },
    methods:{
        handleClick(){
            this.changeColor = '#ff0000'
        }
    }
})
</script> -->

//Estructura Composition API en su version actualizada *Sin el setup*
<!-- <script lang="ts" >
    import {defineComponent, ref} from 'vue'
   export default defineComponent({
    name: 'ClassBindingStyle',
    setup(){
        let changeColor = ref('#fff')
        let handleClick = () => { changeColor.value = '#ff0000'}
        return {changeColor, handleClick}
    }
   })
</script> -->

//Estructura Composition API en su version actualizada *Con el setup*
<script lang="ts" setup>
    import {ref} from 'vue'
    let changeColor = ref('#fff')
    let handleClick = () => {changeColor.value = '#ff0000'}
</script>



<style>
</style>