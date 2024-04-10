<template>
    <div class="container">
        <h3 class="title">{{ counter }}</h3>
        <button @click="addCounter" class="btn">Incrementar</button>
        <button @click="subtractCounter">Decrementar</button>
        <button @click="resetCounter">Reiniciar</button>
    </div>

</template>

<script lang="ts">
import {defineComponent,Ref, ref} from "vue"
export default defineComponent({
name: 'CounterComposition',
setup() {
    let counter:Ref = ref(0);
    const addCounter = ():void => {
       
        counter.value++
       
    }
    let subtractCounter = ():void => {
        if(counter.value > 0){
            counter.value--
}
        
    }
    let resetCounter = ():void => {
        counter.value = 0
    }
    return {counter, addCounter, subtractCounter, resetCounter}
}
})
</script>

<style>
.container{
    display: flex;
    flex-direction: column;
    background-color: gray;
    border-radius: 5px;
}
.title{
    display: flex;
    justify-content: center;
}
.btn{
    border-radius: 5px;
}
.btn:hover{
    cursor: pointer;
}
</style>