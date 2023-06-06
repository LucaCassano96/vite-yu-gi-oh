
<script>
import { store } from "../store.js";

export default{
    name: "AppSearch",
    data() {
        return {
            store,
        }
    }
}

</script>

<template>

    <div class="select">
        <span>Scegli per archetipo:</span>
        <select name="archetype" id="archetype">
            <option value="All">All</option>
            <option @click="$emit('mySelection')" value="Alien">Alien</option>
            <option value="Monster">Monster</option>
            <option value="Noble Knight">Noble Knight</option>

        </select>
    </div>
    


</template>

<style lang="scss" scoped>
@use "src/styles/general.scss" as *;
@use "src/styles/partials/variables.scss" as*;

.select{
    @include container;
    padding: 5px;
    

    select{
        width: 100px;
        margin-left: 10px;
    }
}

</style>