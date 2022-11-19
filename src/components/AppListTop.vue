<script>
import AppCard from './AppCard.vue';

export default {
    name: "AppListTop",
    props: {
        cards: Object
    },
    components: { AppCard }
}
</script>

<template>
    <section class="app-list-top">
        <div class="my-container">
            <h4 class="title">Popular Development Courses</h4>
            <div class="card-row d-flex flex-wrap justify-content-between">
                <AppCard  v-for="n in 6"/>
                <AppCard  v-for="n in 6"/>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.app-list-top {
    margin: 2rem;

    .title {
        font-weight: 600;
        margin-top: 4rem;
    }

    .row-cols-6 {
        margin-top: 2rem;
    }
}

</style>