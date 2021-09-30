<template>
    <div class="comic">
        <a href="#">
            <img :src="details.thumb" :alt="details.series">
            <h4>{{details.series}}</h4>
        </a>
    </div>
</template>

<script>
export default {
    name: 'Comic',
    props: ['details']
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";
.comic {
            padding-top: 2.8125rem;
            width: calc(100% / 6);
            a {
                text-align: center;
                img {
                    height: 10.9375rem;
                    width: 10.9375rem;
                    object-fit: cover;
                    object-position: top;
                }
                h4 {
                    color: #fff;
                    padding-top: 1.25rem;
                    font-weight: normal;
                    font-size: 1.25rem;
                    width: 90%;
                    text-transform: uppercase;
                    text-align: initial;
                }
            }
            
        }

</style>
