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
        <div class="row row-cols-5">
            <div class="col" v-for="character in collection.charactersCard" :key="character.id">
                <Cards :character="character"/>
            </div>
        </div>
    </main>
</template>