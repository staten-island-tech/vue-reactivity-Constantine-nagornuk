<template>
    <div>
        <h2>{{ Destination.name }}</h2>
        h3{{  clicked }}
        <button @click = "increment"> click me </button>
    </div>
</template>

<script setup>
import { ref } from "vue"
    const props = DefineProps({
        Destination:Object
    })

    const clicked = ref(0)
    function  increment(){
        clicked.value++
    }


</script>

<style scoped >
img {
    width:  300px;


}
</style>