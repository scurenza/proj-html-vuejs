<script>
export default {
    name: "AppBannerTop",
    props: {
        imgSrc: String,
        alt: String,
        title: String,
        text: String
    },
    data() {
        return {

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
<section class="my-banner">
    <div class="write d-flex justify-content-center align-items-center">
        <div>
            <h2>{{ title }}</h2>
            <p>{{ text }}</p>
        </div>
    </div>
    <div class="my-image">
        <img :src="getImagePath(`../assets/images/${imgSrc}`)" :alt="alt">
    </div>
</section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

    .my-banner {
        width: 100%;
        height: 40vh;
        margin-top: 280px;

        
        position: relative;

        img {
            height: 100%;
            
        }

        // .write {
        //     z-index: 50;
        //     background: linear-gradient(65deg, $primary-color, $primary-color 90%, white 60%, white);
        //     height: 100%;
        //     width: 70%;

        //     // position: absolute;
        //     // top: 0;
        //     // left: 0;

        //     position: absolute;
        //     z-index: 100;
            
        // }
        // .my-image {
        //     height: 100%;
        //     width: 50%;
        //     // background-image: url(../assets/images/slide-1.jpg);
        //     position: absolute;
        //     z-index: 1;
        //     top: 0;
        //     left: 50%;
        //     background-color: green;
        // }

        .write {
            height: 100%;
            width: 65%;
            background: linear-gradient(65deg, $primary-color, $primary-color 80%, rgba(0, 0, 0, 0.007) 10%, rgba(0, 0, 0, 0));
            position: absolute;
            top: 0;
            left: 0;
            z-index: 10;
            padding:0 14rem;
            color: white;
            

            h2{
                font-size: 3rem;
                font-weight: 800;
            }
            p {
                font-size: 1.5rem;
                
            }
        }

        .my-image {
            height: 100%;
            width: 50%;
            background-color: rgba(0, 128, 0, 0);
            position: absolute;
            top: 0;
            left: 50%;
        }
    }
</style>