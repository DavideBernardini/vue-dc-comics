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
            width: 10.9375rem;
            a {
                img {
                    height: 10.9375rem;
                    width: 100%;
                    object-fit: cover;
                    object-position: top;
                }
                h4 {
                    color: #fff;
                    padding-top: 1.125rem;
                    font-weight: normal;
                    width: 90%;
                    text-transform: uppercase;
                }
            }
            
        }

</style>
