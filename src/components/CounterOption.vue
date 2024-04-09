<template>
<h3>{{ counter }}</h3>
<button @click="addCounter">Incrementar</button>
<button @click="subtractCounter">Decrementar</button>
<button @click="resetCounter">Reiniciar</button>
</template>

<script lang="ts">
//Option API
import { defineComponent } from "vue";
export default defineComponent({
    name: 'CounterOption',
    components: {},
    data(){
let counter = 0;
    return {counter}
},
methods: {
    addCounter(){
        this.counter++;
    },
    subtractCounter(){
        if (this.counter > 0){
            this.counter--;
        }
        
    },
    resetCounter(){
        this.counter = 0;
    }

},
})
</script>

<style>
</style>