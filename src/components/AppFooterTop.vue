<script>
export default {
    name: "AppFooterTop",
    props: {
        about: Object,
        social: Object,
        ad: Object
    },
    methods: {
        getImagePath: function(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section class="footer-top d-flex justify-content-between align-items-center">
        <div class="content text-light">
            <h4>{{about[0].title}}</h4>
            <p>{{about[0].text}}</p>
        </div>
        <div class="content text-light">
            <h4>{{about[1].title}}</h4>
            <p>{{about[1].address}}</p>
            <p>{{about[1].tel}}</p>
            <p>{{about[1].fax}}</p>
            <p class="text-secondary">{{about[1].mail}}</p>
        </div>
        <div class="content">
            <h4 class="text-light">SOCIAL NETWORK</h4> 
            <div class="socials d-flex flex-wrap align-items-center">
                <div v-for="(social, index) in social" :key="index">
                    <a :href="social.href" :class="social.title">
                        <span  v-html="social.icon"></span>
                    </a>
                </div>
            </div>        
        </div>
        <div class="content">
            <img :src="getImagePath(`../assets/images/` + ad[0].imgSrc)" :alt="ad[0].title">
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.footer-top {
    width: 70%;
    margin: 0 auto;
    height: 85%;

    padding: 0 3rem;

    .content {
        height: 70%;
        width: calc(100% / 4 - 35px);

        img {
            width: 100%;
            height: 100%;
        }
    }

    .socials{
        width: 100%;
        height: 80%;
        
        a{
            padding: 1rem;
            border-radius: 100%;
            color: white;
            font-size: 1.5rem;
            margin-right: .5rem;
        }
    }

    .facebook {
        background-color: #3b5998;
    }

    .instagram{
        background-color: #c32aa3;
    }

    .linkedin{
        background-color: #0077b5;
    }

    .pinterest{
        background-color: #bd081c;
    }

    .twitter{
        background-color: #1da1f2;
    }

    .dribbble{
        background-color: #ea4c89;
    }

    .google{
        background-color: #db4437;
    }

    .skipe{
        background-color: #00aff0;
    }
    
}
</style>