
        <!-- {
            "id": 34541863,
            "name": "\"A\" Cell Breeding Device",
            "type": "Spell Card",
            "frameType": "spell",
            "desc": "During each of your Standby Phases, put 1 A-Counter on 1 face-up monster your opponent controls.",
            "race": "Continuous",
            "archetype": "Alien",

            "card_images": [
                {
                    "id": 34541863,
                    "image_url": "https://images.ygoprodeck.com/images/cards/34541863.jpg",
                    "image_url_small": "https://images.ygoprodeck.com/images/cards_small/34541863.jpg",
                    "image_url_cropped": "https://images.ygoprodeck.com/images/cards_cropped/34541863.jpg"
                }
            ],
        
            } -->


<script>

export default {
    name: "AppCard",
    props: {
        details: Object,
    }
}

</script>

<template>
    <div class="card">

        <div class="image">
            <img :src="details.card_images[0].image_url" alt="img">
        </div>

        <div class="description">
            <div class="name">{{ details.name }}</div>
            <div class="archetype">{{ details.archetype }}</div>
        </div>


    </div>
</template>

<style lang="scss" scoped>
@use "src/styles/general.scss" as *;
@use "src/styles/partials/variables.scss" as*;

.card {
    width: 200px;
    min-height: 400px;
    margin:  20px;
    

    .image {
        width: 200px;
        height: 300px;
        
       img{
        width: 200px;
        height: 300px;
        object-fit: cover;
       } 
    }

    .description{
        width: 200px;
        padding: 10px;
        text-align: center;
        background-color: $orange;

        .name{
            color: $white;
            padding: 6px;
        }

    }
}
</style>