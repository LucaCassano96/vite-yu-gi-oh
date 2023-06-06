<script>
import { store } from "../store.js";

import axios from "axios";
import AppCard from './AppCard.vue'
export default {
    name: "AppListCard",
    components: {
        AppCard
    },
    data() {
        return {
            store,
        }
    }
}

</script>

<template>
    <main>

        <div id="cards_container">

            <AppCard v-for="character in store.cards " :details="character" />

        </div>


    </main>
</template>

<style lang="scss" scoped>
@use "src/styles/general.scss" as *;
@use "src/styles/partials/variables.scss" as*;

main {
    width: 100%;
    height: 100vh;
    background-color: $orange;
    padding-top: 80px;

    #cards_container {
        @include container;
        justify-content: space-evenly;
        flex-wrap: wrap;
        min-height: 500px;
        background-color: $white;
    }
}
</style>
