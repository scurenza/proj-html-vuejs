<script>
import AppBannerTop from './AppBannerTop.vue';

export default {
    name: "AppMain",
    components: {
        AppBannerTop,
    },
    data() {
        return {
            bannerTop: {
                imgSrc: "slide-1.jpg",
                alt: "group-photo",
                title: "Udemy Affiliate Sales",
                text: "Monetize your audience and attract new customers with Udemy!" 
            },
        }
    }
}
</script>

<template>
    <section class="main-section"></section>
    <AppBannerTop :img-src="bannerTop.imgSrc" :alt="bannerTop.alt" :title="bannerTop.title"  :text="bannerTop.text"/>
    <AppBannerTop :img-src="bannerTop.imgSrc" :alt="bannerTop.alt" :title="bannerTop.title"  :text="bannerTop.text"/>
    <AppBannerTop :img-src="bannerTop.imgSrc" :alt="bannerTop.alt" :title="bannerTop.title"  :text="bannerTop.text"/>
    <AppBannerTop :img-src="bannerTop.imgSrc" :alt="bannerTop.alt" :title="bannerTop.title"  :text="bannerTop.text"/>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/general.scss" as *;

.main-section {
    overflow-y: scroll;
}
</style>