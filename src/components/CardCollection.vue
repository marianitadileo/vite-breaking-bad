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
        <h3>card collections</h3>
        <ul>
            <li v-for="character in collection" :key="index">{{ character.name }}</li>
        </ul>
        <Cards />
    </main>
    
</template>