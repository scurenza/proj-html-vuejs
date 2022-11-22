<script>
export default {
    name: "AppFooterBottom",
}
</script>

<template>
    <section class="footer-bottom">
        <div class="footer-bottom-container d-flex align-items-center text-center text-light">
            <img src="../assets/images/footer-logo2x-50x56.png" alt="logo">
            <p>Copyright &copy; 2020.</p>
            <a href="">
                MasterStudy.
            </a>
            <p>Theme by</p>
            <a href="">StylenixThemes</a>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.footer-bottom{
    width: 100%;
    height: 15%;
    border-top: 1px solid grey;

    &-container{
        width: 70%;
        height: 100%;
        margin: 0 auto;

        img{
            height: 60%;
            margin-right: 2rem;
        }

        p, a{
            margin-bottom: 0;
            margin-right: .5rem;
        }

        a{
            text-decoration:underline;
        }

    }
}
</style>