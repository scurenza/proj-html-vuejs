<script>
export default {
    name: "AppHeaderMid",
    props: {
        imgSrc: String,
        alt: String
    },
    methods: {
        getImagePath: function(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="header-mid">
        <section class="my-container d-flex justify-content-between">
            <div class="logo d-flex align-items-center justify-content-between">
                <img :src="getImagePath(`../assets/images/${imgSrc}`)" :alt="alt">
            </div>
            <div class="searchbar d-flex align-items-center justify-content-between">
                <div class="d-flex align-items-center justify-content-between">
                    <i class="fa-solid fa-bars"></i>
                    <p class="align-bottom">Category</p>
                </div>
                <div>
                    <input type="text" placeholder="Search Courses">
                    <button class="search">
                        <i class="fa-solid fa-magnifying-glass"></i>
                    </button>
                </div>
            </div>
            <div class="work d-flex align-items-center justify-content-around">
                <a href="/become_instructor">
                    <i class="fa-solid fa-bullhorn"></i>
                    <span>Become an Instructor</span>
                </a>
                <a href="/enterprise">
                    <i class="fa-solid fa-briefcase"></i>
                    <span>For Enterprise</span>
                </a>
            </div>
            <div class="cta d-flex align-items-center justify-content-around">
                <a href="/login">
                    <i class="fa-regular fa-user"></i>
                    <span>Log In</span>
                </a>
                <button class="my-btn">SIGN UP</button>
                <a href="/bookmark">
                    <i class="fa-regular fa-bookmark"></i>
                </a>
            </div>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/general.scss" as *;

.header-mid{
    width: 100%;
    height: 100%;

    
    .logo{
        width: 15%;
    }
    .cta {
        width: 20%;
    }
    .searchbar {
        width: 35%;
        height: 100%;
        color: grey;

        p {
            margin: 0 .3rem;
        }

        input {
            height: 45px;
            width: 320px;
            padding: 1rem;
            border: none;
            font-size: .9rem;

            background-color: #f0f2f5;
        } 

        .search {
            height: 45px;
            width: 50px;
            background-color: $button-color;
            border: none;

            i {
                color: white;
                font-size: .9rem;
            }
        }
    }

    .work {
        width: 24%;
        color: grey;

        i{
            margin-right: .5rem;
        }
    }

    .cta {
        color: grey;
        i {
            font-size: 1.5rem;
            margin-right: .5rem;
        }
    }


}
</style>