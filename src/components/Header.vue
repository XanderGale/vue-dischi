<template>
    <header>
        <img src="../assets/img/logo.png" alt="Spotify Logo">
    </header>
</template>

<script>
export default {
    name: 'Header',
}
</script>

<style scoped lang="scss">
@import '../styles/variables.scss';
    header{
        background-color: $main-color;
        color: white;
        padding: 10px;
        img{
            width: 30px;
            height: 30px;
        }
    }
</style>