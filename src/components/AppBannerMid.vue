<script>
export default {
    name: "AppBannerMid",
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="mid-banner">
        <div class="text">
            <h2>Limitless learning, more possibilites</h2>
            <p>Onilne courses open the opportunity for learning to almost everyone, regardless of their scheduling commitments.</p>
            <button class="my-btn">READ MORE</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.mid-banner {
    
    height: 50vh;
    width: 100%;
    margin-bottom: 6rem;

    background-image: url(../assets/images/bg.png);
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;

    position: relative;

    .text {
        width: 30%;
        position: absolute;
        top: 50%;
        left: 30%;
        transform: translate(-50%, -50%);
    }

    h2{
        font-size: 3rem;
        font-weight: 600;
        margin-bottom: 1rem;
    }

    p{
        font-weight: 500;
        font-size: 1.2rem;
        margin-bottom: 2rem;
    }
}
</style>