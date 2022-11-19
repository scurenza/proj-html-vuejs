<script>
export default {
    name: "AppTools",
    props: {
        tools: Object
}
}
</script>

<template>
    <div class="tool-container">  
            <ul class="d-flex flex-column justify-content-between align-items-center">
                <li v-for="(item, index) in tools" :key="index" :tools="item">                
                    <a :href="item.href" >
                        <span v-html="item.icon"></span>
                    </a>
                </li>
            </ul>
        </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.tool-container {
    width: 65px;
    height: 230px;
    padding: .5rem;

    background-color: white;
    box-shadow: -6px 6px 10px rgba(0, 0, 0, 0.651);

    font-size: 1.3rem;
    ul{
        height: 100%;
        margin: 0;
        padding: 0;
    }
}
</style>