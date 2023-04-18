<script>
import Cards from "./Cards.vue";
import { collection } from "../collection";

export default {
    name: "CardCollection",
    components: {
        Cards
    },
    data() {
        return {
            collection
        }
    }
}
</script>

<template>
    <main class="ms_color">
        <div class="p-3 bg-dark text-light mx-4">Founds cards : {{ this.collection.charactersCard.length }}</div>
        <div v-if="this.collection.charactersCard.length == 0">Loading...</div>
        <div v-else class="row row-cols-5 bg-light mx-4 d-flex justify-content-center"> 
            <div class="col mb-4" v-for="character in collection.charactersCard" :key="character.id">
                <Cards :character="character"/>
            </div>
        </div>
    </main>
</template>