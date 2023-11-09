<script lang="ts" setup>

const pokemon = defineProps(["name", "xp", "height", "image", "loading", "weight", "species"])

</script>
<template>
    <div 
    class="card card-pokemon-selected"
    :class="loading ? '': 'animate__animated animate__flipInY'"
    >
        <img 
        v-if="pokemon.name"
        :src="pokemon.image" 
        class="card-img-top pt-2" 
        alt="..."
        >
        <img 
        v-else
        src="@/assets/egg_pokemon.svg" 
        class="card-img-top pt-2" 
        alt="???"
        >
        <div class="card-body">
            <h5 class="card-title text-center">{{ pokemon.name || '???' }}</h5>
            <hr>
            <div class="row text-center mt-3">
                <section class="col">
                    <section>Peso:</section>
                    <section>{{pokemon.weight || '???'}}</section>
                </section>
                <section class="col">
                    <section>Altura:</section>
                    <section>{{pokemon.height || '???'}}</section>
                </section>
            </div>
            <div class="d-none d-md-block">
                <div class="row text-center mt-3">
                    <section class="col">
                        <section>Xp:</section>
                        <section>{{pokemon.xp || '???'}}</section>
                    </section>
                    <section class="col">
                        <section>Espécie:</section>
                        <section>{{pokemon.species || '???'}}</section>
                    </section>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card-pokemon-selected{
    height: 75vh;
    background: rgb(72,63,251);
    background: radial-gradient(circle, rgba(251, 223, 63, 0.8) 0%, rgba(252, 70, 70, 0.8) 100%);
}

.card-pokemon-selected img {
        height: 250px;
    }

@media (max-width: 768px) {
    .card-pokemon-selected{
        height: 30vh;
        width: 40%;
        margin: 0 auto 10px auto;
    }

    .card-pokemon-selected img {
        height: 100px;
    }
}
</style>