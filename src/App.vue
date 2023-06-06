<script>
import { store } from "./store.js";
import axios from "axios";
import AppHeader from './components/AppHeader.vue'
import AppListCard from './components/AppListCard.vue'
import AppSearch from './components/AppSearch.vue'
export default {
  components: {
    AppHeader,
    AppListCard,
    AppSearch,
  },
  data() {
    return {
      store,
    }
  },
  methods: {
    getCharacters() {
      axios.get(store.apiURL)
        .then(res => {
          store.cards = res.data.data;
        }
        )
        .catch(err => {
          console.log(err);
        })
    }
  },
  created() {
    this.getCharacters();
  }
}
</script>

<template>
  <AppHeader />
  <main>
    <AppSearch />
    <AppListCard />
  </main>
  
</template>

<style lang="scss">
@use "./styles/partials/variables.scss" as*;
@use "./styles/general.scss" as*;
</style>
