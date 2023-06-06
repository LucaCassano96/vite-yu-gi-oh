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

      let myUrl = store.apiURL;

      if (store.option !== "All") {
        myUrl += `?${store.apiArchetypeParameter}=${store.option}`
      }

      axios.get(myUrl)
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
    <AppSearch @mySelection="getCharacters" />
    <AppListCard />
  </main>
</template>

<style lang="scss">
@use "./styles/partials/variables.scss" as*;
@use "./styles/general.scss" as*;
</style>
