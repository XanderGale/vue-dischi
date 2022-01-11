<template>
    <div class="single-item">
        <img :src="itemDetails.poster" :alt="itemDetails.title + ' image'">

        <h3>{{ itemDetails.title }}</h3>

        <h4>{{ itemDetails.author }}</h4>
        <h5>{{ itemDetails.year }}</h5>
    </div>
</template>

<script>
export default {
    name: "SingleItem",
    props: {
        itemDetails: Object,
    }
}
</script>

<style scoped lang="scss">
@import '../styles/variables.scss';
    .single-item{
        background-color: $main-color;
        padding: 10px;
        margin: 10px;
    
        width: calc((100% / 5) - 20px);
        min-height: 350px;

        color: #7f7f7e;

        text-align: center;

        display: flex;
        flex-flow: column nowrap;
        justify-content: flex-start;
        align-items: center;
        h3{
            margin: 20px 0;
            color: white;
            text-transform: uppercase;
        }
    }
</style>