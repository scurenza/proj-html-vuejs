<script>
import AppBannerTop from './AppBannerTop.vue';
import AppTools from './AppTools.vue';
import AppListTop from './AppListTop.vue';

export default {
    name: "AppMain",
    components: {
        AppBannerTop,
        AppTools,
        AppListTop,
    },
    data() {
        return {
            bannerTop: {
                imgSrc: "slide-1.jpg",
                alt: "group-photo",
                title: "Udemy Affiliate Sales",
                text: "Monetize your audience and attract new customers with Udemy!" 
            },
            tools : [
                {
                    icon: "<i class=\"fa-solid fa-desktop\"></i>",
                    href: "/computer"
                },
                {
                    icon: "<i class=\"fa-solid fa-life-ring\"></i>",
                    href: "/life-ring"
                },
                {
                    icon: "<i class=\"fa-solid fa-wrench\"></i>",
                    href: "/tool"
                },
                {
                    icon: "<i class=\"fa-solid fa-cart-shopping\"></i>",
                    href: "/shopping-cart"
                },
                {
                    icon: "<i class=\"fa-solid fa-mobile-screen\"></i>",
                    href: "/phone"
                },
            ],
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
                    discountedPrice: ""

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

                },
            ]

            
        }
    }
}
</script>

<template>
    <section class="main-section">
        <AppBannerTop :img-src="bannerTop.imgSrc" :alt="bannerTop.alt" :title="bannerTop.title"  :text="bannerTop.text"/>
        <AppTools class="tools" :tools="tools"/>
        <AppListTop />
    </section>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/general.scss" as *;

.main-section {
    overflow-y: scroll;
    position: relative;
    width: 100%;
    height: 100vh;

    .tools{
        position: fixed;
        bottom: 5%;
        right: 0;
        transform: translate(-26%, 0);
    }
}
</style>