<script>
import AppHeader from "./components/AppHeader.vue";
import CardCollection from "./components/CardCollection.vue";
import Cards from "./components/Cards.vue";
import axios from "axios";
import { collection } from "./collection";

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
    axios.get(collection.apiURL).then((resp) => {
      this.collection.charactersCard = resp.data.data;
    })
  }
}
</script>

<template>
  <AppHeader title="Yu-Gi-Oh Api"/>
  <CardCollection />
  <Cards />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>