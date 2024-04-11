<template>
    <div class="container">
        <h3 class="title">{{ counter }}</h3>
        <button @click="addCounter" class="btn">Incrementar</button>
        <button @click="subtractCounter">Decrementar</button>
        <button @click="resetCounter">Reiniciar</button>
    </div>
</template>

//Composition API
<script lang="ts" setup>

    import {Ref, ref} from "vue"

    let counter:Ref = ref(0);

    let addCounter = ():void => {
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