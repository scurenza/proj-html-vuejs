<script>
export default {
    name: "AppTestimonial",
    data() {
        return {
            title: "Investing for Your Future",
            text: "It is no exxaggeration to say this MasterStudy experience was transformative-both professionally and personally. This workshop will long remain a high point of my life. Thanks again... I am feeling energized and eager to start teaching my class next week. I can't wait to use all of my teaching tools. I will absolutely recommend this workshop to other educators!",
            name: "Linda Green",
            occupation: "Product Manager, Apple Inc"
        }
    }

}
</script>

<template>
    <section class="testimonial">
        <div class="text-container d-flex justify-content-center align-items-center">
            <div>
                <h2>{{title}}</h2>
                <p class="text mb-5">{{text}}</p>
                <p class="name">{{name}}</p>
                <p class="occupation">{{occupation}}</p>
            </div>
            <div class="triangle">
                <i class="fa-solid fa-play"></i>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.testimonial{
    height: 65vh;
    width: 100%;
    background-image: url(../assets/images/testimonial-1-1917x640-1-1914x639.jpg);
    object-fit: cover;
    object-position: left;

    position: relative;

    .triangle i{
        color: white;
        z-index: 2;
        position: absolute;
        font-size: 2rem;

        top: 50%;
        right: -22px;
        
    }
    .text-container{
        width: 40%;
        height: 75%;
        background-color: white;
        padding: 0 5rem;

        position: absolute;
        top: 30%;
        left: 23%;
        transform: translate(-20%, -20%);

        z-index: 2;

        h2{
            font-size: 2.1rem;
            margin-bottom: 2rem;
        }
        .text{
            font-size: 1.1rem;
            font-weight: 200;

            color: rgba(0, 0, 0, 0.459);
        }

        .name{
            font-weight: 700;
            margin: 0;
        }

        .occupation{
            font-size: .9rem;
            color: rgba(0, 0, 0, 0.659);
        }

    }
}
</style>