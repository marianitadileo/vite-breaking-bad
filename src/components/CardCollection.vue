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
        <div v-for="character in collection.charactersCard" :key="character.id">
            <Cards :character="character"/>
        </div>
      
    </main>
</template>