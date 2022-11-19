<script>
export default {
    name: "AppHeaderBottom",
    props: {
        actionTitle: String,
        actionIcon: String
    }
}
</script>

<template>

            <ul>
                <li>
                    <a href="" class="d-flex">
                        <span v-html="actionIcon"></span>
                        <p>{{ actionTitle }}</p>
                    </a>
                </li>
            </ul>
           
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;


    a{
        color: white;
    }
        span{
            margin-right: 1rem;
        }


</style>