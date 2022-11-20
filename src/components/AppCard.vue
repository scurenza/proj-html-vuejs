<script>
export default {
    name: "AppCard",
    props: {
        cards: Object
    },
    methods: {
        getImagePath: function(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="card-container" v-for="index in 6" :key="index" >
        <div class="image">
            <img :src="getImagePath(`../assets/images/${cards[index].imgSrc}`)" alt="">
        </div>
        <div class="card-description">
            <div class="category mt-1">
                <span> {{cards[index].category}} ></span>
            </div>
            <div class="card-text mt-2 pb-3">
                {{cards[index].text}} 
            </div>
            <div class="card-bottom mt-3 d-flex justify-content-between align-items-center">
                <div class="vote">
                    <img src="../assets/images/starfull.svg" alt="">
                    <img src="../assets/images/starfull.svg" alt="">
                    <img src="../assets/images/starfull.svg" alt="">
                    <img src="../assets/images/starfull.svg" alt="">
                    <img src="../assets/images/staremptyl.svg" alt="">
                </div>
                <div class="price d-flex flex-column">
                    <span class="original-price">${{cards[index].price}}</span>
                    <span class="discount">${{cards[index].discountedPrice}}</span>
                </div>
            </div>
        </div>
    </div>
    
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.card-container {
    min-height: 350px;
    width: calc(100% / 6 - 10px);
    margin: 20px 0;

    border: 1px solid rgba(128, 128, 128, 0.459);

    .card-description {
        padding: 1.2rem;
        
        .category span {
            color: grey;
            font-size: .8rem;
        }
        .card-text {
            border-bottom: 1px solid rgba(128, 128, 128, 0.5);
        }

        .price{
            .original-price {
                text-decoration: line-through;
                color: grey;
                font-size: .75rem;
            }

            .discount {
                font-size: 1.1rem;
                font-weight: 600;
            }
        }
    }
}
</style>