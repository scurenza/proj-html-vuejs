<script>
import AppFooterTop from './AppFooterTop.vue';
import AppFooterBottom from './AppFooterBottom.vue';

export default {
    name: "AppFooter",
    components: {
        AppFooterTop,
        AppFooterBottom
    },
    data() {
        return {
            footerAbout: [
                {
                    title: "ABOUT",
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Architecto, velit reiciendis maxime neque voluptas suscipit alias tenetur perspiciatis recusandae vitae?"
                },
                {
                    title: "CONTACT",
                    address: "USA, California 20, First Avenue, California",
                    tel: "+1 212 458 300 32",
                    fax: "+1 212 375 24 14",
                    mail: "info@masterstudy.com"
                }
            ],
            socials: [
                {
                    title: "facebook",
                    icon: "<i class=\"fa-brands fa-facebook\"></i>",
                    href: "/facebook"
                },
                {
                    title: "instagram",
                    icon: "<i class=\"fa-brands fa-instagram\"></i>",
                    href: "/instagram"
                },
                {
                    title: "linkedin",
                    icon: "<i class=\"fa-brands fa-linkedin\"></i>",
                    href: "/linkedin"
                },
                {
                    title: "pinterest",
                    icon: "<i class=\"fa-brands fa-pinterest\"></i>",
                    href: "/pinterest"
                },
                {
                    title: "twitter",
                    icon: "<i class=\"fa-brands fa-twitter\"></i>",
                    href: "/twitter"
                },
                {
                    title: "dribbble",
                    icon: "<i class=\"fa-brands fa-dribbble\"></i>",
                    href: "/dribbble"
                },
                {
                    title: "google",
                    icon: "<i class=\"fa-brands fa-google-plus\"></i>",
                    href: "/google+"
                },
                {
                    title: "skipe",
                    icon: "<i class=\"fa-brands fa-skype\"></i>",
                    href: "/skipe"
                }
            ],
            ad: [
                {
                    title: "udemy ad",
                    imgSrc: "Top-udemy-courses-90-percent-off.jpg"
                }
            ]
        }
    }
}
</script>

<template>
    <section class="footer">
        <AppFooterTop :about="footerAbout" :social="socials" :ad="ad"/>
        <AppFooterBottom />
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.footer{
    width: 100%;
    height: 45vh;
    background-color: $secondary-color;
}
</style>