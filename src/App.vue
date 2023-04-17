<script>
import AppHeader from "./components/AppHeader.vue";
import CardCollection from "./components/CardCollection.vue";
import Cards from "./components/Cards.vue";
import axios from "axios";



export default {
  components: {
    AppHeader,
    CardCollection,
    Cards
  }, 
  data() {
    return {
      collection
    }
  },
  mounted() {
        axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0").then((resp) => {
            this.collection.characterCards = resp.data.data;
    })
  }
}
</script>

<template>
  <AppHeader title="Yu-Gi-Oh Api"/>
  <CardCollection />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>