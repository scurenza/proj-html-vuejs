<script>
import AppHeaderBottom from './AppHeaderBottom.vue';
import AppHeaderMid from './AppHeaderMid.vue';

export default {
    name: "AppHeader",
    components: {
        AppHeaderBottom,
        AppHeaderMid
    },
    data() {
        return {
            links: [
                {
                    title: "Home",
                    href: "/home",
                    active: false
                },
                {
                    title: "Pages",
                    href: "/pages",
                    active: false
                },
                {
                    title: "Course Formats",
                    href: "/course_formats",
                    active: false
                },
                {
                    title: "Courses",
                    href: "/courses",
                    active: false
                },
                {
                    title: "Demos",
                    href: "/demos",
                    active: false
                }
            ],
            socials: [
                {
                    title: "Facebook",
                    icon: "<i class=\"fa-brands fa-facebook\"></i>",
                    href: "/facebook"
                },
                {
                    title: "Twitter",
                    icon: "<i class=\"fa-brands fa-twitter\"></i>",
                    href: "/twitter"
                },
                {
                    title: "Instagram",
                    icon: "<i class=\"fa-brands fa-instagram\"></i>",
                    href: "/instagram"
                },
                {
                    title: "Linkedin",
                    icon: "<i class=\"fa-brands fa-linkedin\"></i>",
                    href: "/linkedin"
                },
                {
                    title: "Google+",
                    icon: "<i class=\"fa-brands fa-google-plus\"></i>",
                    href: "/google+"
                },
                {
                    title: "Youtube",
                    icon: "<i class=\"fa-brands fa-youtube\"></i>",
                    href: "/youtube"
                }
            ],
            actions: [
                {
                    title: "Business",
                    icon: "<i class=\"fa-solid fa-chart-line\"></i>"
                },
                {
                    title: "Design",
                    icon: "<i class=\"fa-solid fa-palette\"></i>"
                },
                {
                    title: "Development",
                    icon: "<i class=\"fa-solid fa-gear\"></i>"
                },
                {
                    title: "Lifestyle",
                    icon: "<i class=\"fa-regular fa-face-smile\"></i>"
                },
                {
                    title: "Office Productivity",
                    icon: "<i class=\"fa-solid fa-boxes-packing\"></i>"
                }
            ],
            logo: [
                {
                    imgSrc: "MasterStudy.svg",
                    alt: "MasterStudy Logo"
                }
            ]
        };
    }
}
</script>

<template>
    <header class="header">
        <section class="header-top">
            <div class="my-container d-flex justify-content-between">
                <div class="header-top-left">
                    <a href="/lang">
                        <p>English <i class="fa-solid fa-chevron-down"></i></p>
                    </a>
                </div>
    
                <div class="header-top-right d-flex">
                    <div class="links">
                        <ul class="d-flex">
                            <li v-for="(item, index) in links" :key="index">
                                <a :href="item.href" :class="{'active' : item.active}">{{ item.title }}</a>
                            </li>
                        </ul>
                    </div>
                    
                    <div class="socials">
                        <ul class="d-flex">
                            <li v-for="(item, index) in socials" :key="index">
                                <a :href="item.href" v-html="item.icon"></a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
        <section class="header-mid">
            <AppHeaderMid v-for="(item, index) in logo" :key="index" :imgSrc="item.imgSrc" :alt="item.alt" />
        </section>
        <section class="header-bottom d-flex">
            <div class="header-bottom-container d-flex justify-content-between">
                <AppHeaderBottom class="my-header-bottom" v-for="(item, index) in actions" :key="index" :actionTitle="item.title" :actionIcon="item.icon" />
            </div>
        </section>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.header {
    width: 100%;
    height: 25vh;

    position: fixed;
    top: 0;
    left: 0;
    z-index: 400;



    &-top {
        width: 100%;
        height: 4vh;
        line-height: 4vh;
        border-bottom: 1px solid grey;
        color: rgba(128, 128, 128, 0.738);
        font-size: .9rem;
        background-color: white;

        &-left:hover i{
            transform: rotate(180deg);
        }

        .links li{
            margin-right: 1.5rem;
        }

        .socials li {
            margin-right: .75rem;
            font-size: 1.1rem;
        }
    }

    &-mid {
        width: 100%;
        height: 9vh;
        background-color: white;
    }

    &-bottom {
        width: 100%;
        height: 6vh;
        line-height: 6vh;
        background-color: $secondary-color;

    }

    &-bottom-container {
        width: 55%;
        height: 8vh;
        margin: 0 auto;
    }
    .my-header-bottom {
        font-size: 1.1rem;
    }
}
</style>