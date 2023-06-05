<script>

export default {
    name: "AppHeader"
}

</script>

<template>
    <header>

       
        <!-- title -->

        <div id="container">

            <div class="logo">

                <img src="https://ygoprodeck.com/cdn-cgi/image/width=150/https://images.ygoprodeck.com/assets/images/ygoprodeck_logo.png" alt=""> 

            </div>

            <h1>YU-GI-OH API</h1>
            

        </div>

    </header>
</template>

<style lang="scss" scoped>
@use "src/styles/general.scss" as *;
@use "src/styles/partials/variables.scss" as*;

header {
    width: 100%;
    height: 80px;
    display: flex;

   

    #container {
        @include container;
        height: 80px;

        .logo{
        width: 100px;
        margin:0 15px;
        img{
            width: 100px;
        }
    }
    }
}
</style>
