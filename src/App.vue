<script>
import AppHeader from "./components/AppHeader.vue";
import CardCollection from "./components/CardCollection.vue";
import Cards from "./components/Cards.vue";
import axios from "axios";
import { collection } from "./collection";
import SearchBar from "./components/SearchBar.vue";

export default {
  components: {
    AppHeader,
    CardCollection,
    Cards,
    SearchBar
  }, 
  data() {
    return {
      collection
    }
  },
  mounted() {
    this.optionsFilter();
  }, 
  methods: {
    optionsFilter() {
      if (this.collection.selectedStatus.length > 0) {
        this.collection.apiURL += `&archetype=${this.collection.selectedStatus}`
      }
      axios.get(this.collection.apiURL, {
        params: {
          status: this.collection.selectedStatus
        }
      }).then((resp) => {
      this.collection.charactersCard = resp.data.data;
      console.log(collection.charactersCard);
    })
    }
  }
}
</script>

<template>
  <AppHeader title="Yu-Gi-Oh Api"/>
  <SearchBar @filter="optionsFilter" />
  <CardCollection />
</template>

<style lang="scss">
@use "./style/general.scss";
</style>