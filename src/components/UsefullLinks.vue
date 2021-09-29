<template>
    <section class="usefull_links">
        <ul>
            <li v-for="(link, index) in links" :key="index">
                <a href="#">
                    <img :src="require(`@/assets/img//${link.icon}`)" :alt="link.iconAlt">
                    <span>{{link.text}}</span>
                </a>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    name: 'UsefullLinks',
    data() {
        return {
            links: [
                {
                    text: 'DIGITAL COMICS',
                    icon: 'buy-comics-digital-comics.png',
                    iconAlt: 'icon comic'
                },
                {
                    text: 'DC MERCHANDISE',
                    icon: 'buy-comics-merchandise.png',
                    iconAlt: 'icon t-shirt'
                },
                {
                    text: 'SUBSCRIPTION',
                    icon: 'buy-comics-subscriptions.png',
                    iconAlt: 'icon cards'
                },
                {
                    text: 'COMIC SHOP LOCATOR',
                    icon: 'buy-comics-subscriptions.png',
                    iconAlt: 'icon pin'
                },
                {
                    text: 'DC POWER VISA',
                    icon: 'buy-dc-power-visa.svg',
                    iconAlt: 'icon credit card'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import "@/assets/style/variables.scss";

.usefull_links {
    height: 9.375rem;
    background-color: $mainColor;
    display: flex;
    ul {
        margin: auto;
        li {
            display: inline-block;
            padding: 2.1875rem;
            a {
                color: #fff;
                img {
                    height: 3.4375rem;
                    vertical-align: middle;
                    padding-right: .625rem;
                }
            }
        }
        li:last-child img {
                    height: 45px;
                }
    }
    
}
</style>