<script>

export default {
    name: "AppHeader"
}

</script>

<template>
    <header>

        <div id="container">

            <h1>YU-GI-OH API</h1>

        </div>

    </header>
</template>

<style lang="scss" scoped>
/* @use ".styles/partials/variables.scss" as*; */
@use "src/styles/general.scss" as *;
@use "src/styles/partials/variables.scss" as*;

header {
    width: 100%;
    height: 80px;

    #container {
        @include container;
    }
}
</style>
