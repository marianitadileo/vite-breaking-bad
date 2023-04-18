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
    <div class="text-center card text-bg-warning" style="width: 18rem;">
        <img :src="character.card_images[0].image_url" alt="" class="card-img-top">
        <div class="card-body">
            <h3 class="card-title">{{ character.name }}</h3>
            <h3 class="card-title">{{ character.archetype }}</h3>
        </div>
    </div>
</template>

<style scoped lang="scss">
</style>

