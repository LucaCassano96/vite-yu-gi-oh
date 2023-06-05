<script>

export default {
    name: "AppMain.vue"
}

</script>

<template>

   <main>

        <div id="cards_container">

        </div>


   </main>

</template>

<style lang="scss" scoped>
@use "src/styles/general.scss" as *;
@use "src/styles/partials/variables.scss" as*;

main{
    width: 100%;
    height: 100vh;
    background-color: $orange;
    padding-top: 80px;

    #cards_container{
        @include container;
        min-height: 500px;
        background-color: $white;
    }
}

</style>
