<script>
import AppBannerTop from './AppBannerTop.vue';
import AppTools from './AppTools.vue';
import AppListTop from './AppListTop.vue';
import AppBannerMid from './AppBannerMid.vue';
import AppListMid from './AppListMid.vue';
import AppNewsletter from './AppNewsletter.vue';

export default {
    name: "AppMain",
    components: {
        AppBannerTop,
        AppTools,
        AppListTop,
        AppBannerMid,
        AppListMid,
        AppNewsletter
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
        <AppBannerMid />
        <AppListMid />
        <AppNewsletter />
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
        z-index: 10;
    }
}
</style>