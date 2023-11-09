<script setup lang="ts">

const props = defineProps(['name', 'urlBaseSvg'])
</script> 

<template>
    <div class="col-4 col-md-6 col-xl-3">
        <div class="card cardListPokemon mb-3 p-2">
            <p class="text-center">{{ props.name }}</p>
            <img 
            :src="urlBaseSvg" 
            class="card-img-top" 
            alt=""
            height="80"
            />
        </div>
    </div>
</template>

<style scoped>
.cardListPokemon{
    background: rgb(72,63,251);
    background: radial-gradient(circle, rgba(72,63,251,0.6) 0%, rgba(70,252,244,0.2) 100%);
    cursor: pointer;
}
.cardListPokemon:hover{
    background: rgb(72,63,251);
    background: radial-gradient(circle, rgba(72,63,251,0.6) 0%, rgba(70,252,244,0.4) 100%);
}
.cardListPokemon img:hover{
    padding: .1rem;
}
</style>