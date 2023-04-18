<script>
import { collection } from '../collection';

export default {
    name: "SearchBar",
    data() {
        return {
            collection,
            statusOptions: ["Alien", "Ally of Justice", "Ancient Gear"]
        }
    }
}
</script>

<template>
    <div class="container">
        <select name="status" id="status" v-model="collection.selectedStatus" @change="$emit('filter')">
            <option :value="status" v-for="status in statusOptions">{{ status }}</option>
        </select>
    </div>
</template>