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
    <main class="bg-warning">
        <div class="p-3 bg-dark text-light mx-4">Founds {{ collection.charactersCard.length }} cards</div>
        <div v-if="collection.charactersCard.length === 0">Loading...</div>
        <div v-else class="row row-cols-5 bg-light mx-4"> 
            <div class="col m-4" v-for="character in collection.charactersCard" :key="character.id">
                <Cards :character="character"/>
            </div>
        </div>
    </main>
</template>