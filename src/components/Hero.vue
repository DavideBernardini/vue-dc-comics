<template>
    <div class="hero titans" :style="`background-image: url(${bgImage})`"></div>
</template>

<script>
export default {
    name: 'Hero',
    props: ['bgImage']
}

</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.hero.titans {
    height: 25rem;
    background-size: cover;
}
</style>



