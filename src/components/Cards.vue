<script>
import { collection } from '../collection';

export default {
    name: "Cards",
    data() {
            return {
               collection
            }
    },
    props: {
      character: Object
    }
}
</script>

<template>
    <div class="text-center container">
        <img :src="character.image" alt="">
        <h3>{{ character.name }}</h3>
    </div>
</template>

<style scoped lang="scss">
</style>

