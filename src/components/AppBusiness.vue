<script>
export default {
    name: "AppBusiness",
    data() {
        return {
            links: [
                {
                    imgSrc: "image_box_1-221x231.png",
                    title: "Become an Instructor",
                    text: "Teach what you love. Masterstudy gives you the tools to create a course.",
                    button: "START TEACHING"
                },
                {
                    imgSrc: "image_box_2-234x231.png",
                    title: "Access For Business",
                    text: "Het unlimited access to 2,500 of top courses for your team.",
                    button: "DOING BUSINESS"
                }
            ]
        }
    },
    methods: {
        getImagePath: function(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="business">
        <div class="business-container d-flex align-items-center justify-content-between">
            <div class="link d-flex align-items-center justify-content-evenly">
                <div class="image">
                    <img :src="getImagePath(`../assets/images/` + links[0].imgSrc)" alt="">
                </div>
                <div class="text">
                    <h2 class="mb-2">{{links[0].title}}</h2>
                    <p class="mb-4">{{links[0].text}}</p>
                    <button class="my-btn">{{links[0].button}}</button>
                </div>
            </div>
            <div class="link d-flex align-items-center justify-content-evenly">
                <div class="image">
                    <img :src="getImagePath(`../assets/images/${links[1].imgSrc}`)" alt="">
                </div>
                <div class="text">
                    <h2 class="mb-2">{{links[1].title}}</h2>
                    <p class="mb-4">{{links[1].text}}</p>
                    <button class="my-btn">{{links[1].button}}</button>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.business {
    height: 50vh;
    width: 100%;

    &-container{
        height: 100%;
        width: 90%;
        margin: 0 auto;

        .text {
            width: 50%;

            p{
                color: rgba(128, 128, 128, 0.659);
                
            }
        }
        .link{
            height: 70%;
            width: calc(100% / 2 - 10px);

            border: 1px solid rgba(128, 128, 128, 0.319);
        }
    }
}
</style>