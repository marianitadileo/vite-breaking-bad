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
    <div class="text-center card ms_color" style="width: 18rem;">
        <img :src="character.card_images[0].image_url" alt="" class="card-img-top">
        <div class="card-body ms-card">
            <h3 class="card-title fs-5 text-uppercase text-light">{{ character.name}}</h3>
            <h3 class="card-title fs-5 pt-3">{{ character.archetype }}</h3>
        </div>
    </div>
</template>

<style scoped lang="scss">
.ms-card {
    height: 150px;
    
}
</style>

