<script>
import AppCard from './AppCard.vue';

export default {
    name: "AppListMid",
    components: { AppCard },
    data() {
        return {
            cards: [
                {
                    imgSrc: "895786_7b4b_2-272x161.jpg",
                    category: "Development",
                    text: "The complete iOS 10 & Swift 3 Developer Course",
                    vote: 4,
                    price: 199.99,
                    discountedPrice: 100,
                    

                },
                {
                    imgSrc: "246154_d8b0_3-272x161.jpg",
                    category: "Development",
                    text: "Web Design for Beginners: Real World Coding in HTML & CSS",
                    vote: 5,
                    price: 129.99,
                    discountedPrice: 65

                },
                {
                    imgSrc: "752950_b773-272x161.jpg",
                    category: "Development",
                    text: "GitHub Ultimate: Master Git and GitHub - Beginner to Expert",
                    vote: 4,
                    price: 99.99,
                    discountedPrice: 50

                },
                {
                    imgSrc: "1253188_58f7_2-272x161.jpg",
                    category: "Development",
                    text: "The Complete iOS 11 & Swift Developer Course - Build 20 Apps",
                    vote: 4,
                    price: 199.99,
                    discountedPrice: 100

                },
                {
                    imgSrc: "919872_ed54_6-272x161.jpg",
                    category: "Development",
                    text: "Android Java Masterclass - Become an App Developer",
                    vote: 4,
                    price: 99.99,
                    discountedPrice: 50

                },
                {
                    imgSrc: "951684_9c1a_2-272x161.jpg",
                    category: "Development",
                    text: "Xamarin Forms: Build Native Cross-platform Apps with C#",
                    vote: 4,
                    price: 109.99,
                    discountedPrice: 95

                },
                {
                    imgSrc: "1561458_7f3b-272x161.jpg",
                    category: "Design",
                    text: "CSS - The Complete Guide 2020 (incl. Flexbox, Grid & Sass)",
                    vote: 5,
                    price: 199.99,
                    discountedPrice: 100

                },
                {
                    imgSrc: "1208228_d61c_4-272x161.jpg",
                    category: "Design",
                    text: "Digitally Painting Light and Color: Amateur to Master",
                    vote: 4,
                    price: 139.99,
                    discountedPrice: 70

                },
                {
                    imgSrc: "186792_41e4_4-272x161.jpg",
                    category: "Arts & Crafts",
                    text: "Become an Arabic Calligraphy Artist from Scratch",
                    vote: 5,
                    price: 199.99,
                    discountedPrice: 199.99

                },
                {
                    imgSrc: "1776542_30b1-272x161.jpg",
                    category: "Google",
                    text: "Google Searching Ninja!",
                    vote: 4,
                    price: 89.99,
                    discountedPrice: 45

                },
                {
                    imgSrc: "949316_2a64_11-272x161.jpg",
                    category: "Arts & Crafts",
                    text: "Foundations for Mastering Watercolor Painting",
                    vote: 5,
                    price: 19.99,
                    discountedPrice: 10

                },
                {
                    imgSrc: "381588_2e6d_4-272x161.jpg",
                    category: "Arts & Crafts",
                    text: "The Colored Pencil Drawing Course",
                    vote: 4,
                    price: 34.99,
                    discountedPrice: 18

                },
                {
                    imgSrc: "838056_611a_3-272x161.jpg",
                    category: "Arts & Crafts",
                    text: "Paint Realistic Watercolor and Botanicals - STUDIO BASICS",
                    vote: 4,
                    price: 69.99,
                    discountedPrice: 35

                },
                {
                    imgSrc: "1414956_d944_15-272x161.jpg",
                    category: "Arts & Crafts",
                    text: "Mastering Brushstrokes - Part 1",
                    vote: 5,
                    price: 19.99,
                    discountedPrice: 10

                },
                {
                    imgSrc: "1109398_4c13-272x161.jpg",
                    category: "Arts & Crafts",
                    text: "Paint Realistic Watercolour and Botanicals - MAGNOLIAS",
                    vote: 5,
                    price: 69.99,
                    discountedPrice: 35

                }
            ]
            
        }
    }
}
</script>

<template>
    <section class="app-list-top">
        <div class="my-container">
            <h2 class="title text-center">Recent courses</h2>
            <div class="categories d-flex justify-content-between align-items-center">
                <a href="" class="active">
                    <span>All Categories</span>
                </a>
                <a href="">
                    <span>Business</span>
                </a>
                <a href="">
                    <span>Design</span>
                </a>
                <a href="">
                    <span>Development</span>
                </a>
                <a href="">
                    <span>IT & Software</span>
                </a>
                <a href="">
                    <span>Lifestyle</span>
                </a>
                <a href="">
                    <span>Marketing</span>
                </a>
                <a href="">
                    <span>Office Productivity</span>
                </a>
            </div>
            <div class="card-row mb-5 d-flex flex-wrap justify-content-between">
                <AppCard v-for="n in 12" :key="n" :card="cards[n]" />
            </div>
            <div class="button text-center">
                <button class="my-btn">SHOW ALL</button>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.app-list-top {
    margin: 2rem 0 4rem;

    .title {
        font-weight: 700;
        font-size: 3rem;
        margin: 4rem 0 3rem;
    }

    .row-cols-6 {
        margin-top: 2rem;
    }

    .categories{
        width: 80%;
        margin: 0 auto 1rem;

        .active{
            background-color: #f0f4fa;
            padding: .6rem 1rem;
            border-radius: 20px;
        }

        span {
            color: grey;
        }
    }
}

</style>