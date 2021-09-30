<template>
    <footer>
        <div class="footer_top">
            <div class="container">
                <div class="links">
                    <div class="col">
                        <h3>{{list1.title}}</h3>
                        <ul>
                            <li v-for="(link, index) in list1.links" :key="index">
                                <a href="#">{{link}}</a>
                            </li>
                        </ul>
                        <h3>{{list2.title}}</h3>
                        <ul>
                            <li v-for="(link, index) in list2.links" :key="index">
                                <a href="#">{{link}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <h3>{{list3.title}}</h3>
                        <ul>
                            <li v-for="(link, index) in list3.links" :key="index">
                                <a href="#">{{link}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        <h3>{{list4.title}}</h3>
                        <ul>
                            <li v-for="(link, index) in list4.links" :key="index">
                                <a href="#">{{link}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="logo_bg">
                    <img src="../assets/img/dc-logo-bg.png" alt="logo DC comics big">
                </div>
            </div>
        </div>
        <div class="footer_bottom">
            <div class="container">
                <a href="#" class="sign_up">SIGN-UP NOW!</a>
                <div class="social">
                    <h3>
                        FOLLOW US
                    </h3>
                    <ul>
                        <li v-for="(link, index) in social" :key="index">
                            <a href="#">
                                <img :src="require(`../assets/img//${link.icon}`)" :alt="link.alt">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            list1: {
                title: 'DC COMICS',
                links: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
            },
            list2: {
                title: 'SHOP',
                links: ['Shop DC', 'Shop DC Collectibles']
            },
            list3: {
                title: 'DC',
                links: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscription', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help',
                'Contact Us']
            },
            list4: {
                title: 'SITES',
                links: ['DC', 'MAD Magazine', 'DC Kids', 'DC Uiverse', 'DC Power Visa']
            },
            social: [
                {
                    icon: 'footer-facebook.png',
                    alt: 'facebook icon'
                },
                {
                    icon: 'footer-twitter.png',
                    alt: 'twitter icon'
                },
                {
                    icon: 'footer-youtube.png',
                    alt: 'youtube icon'
                },
                {
                    icon: 'footer-pinterest.png',
                    alt: 'pinterest icon'
                },
                {
                    icon: 'footer-periscope.png',
                    alt: 'periscope icon'
                }
            ]
        }
        }
    }
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.footer_top {
    height: 23.125rem;
    background-image: url('../assets/img/footer-bg.jpg');
    overflow: hidden;
    .links {
        display: flex;
        .col:nth-child(2) {
            padding: 0 1.875rem;
        }
        h3 {
            color: #fff;
            font-size: 1.25rem;
        }
        h3:nth-child(3) {
            padding-top: 1.5625rem;
        }
        ul {
            padding-top: 1.5625rem;
            a {
                color: #959595;
            }
        }
    }
}
.footer_bottom {
    height: 6.875rem;
    background-color: #303030;
    .sign_up {
            font-size: .9375rem;
            color: #fff;
            border: 1px solid $mainColorDarker;
            padding: .875rem .75rem;
            font-family: Arial, Helvetica, sans-serif
        }
    .social {
        h3 {
            display: inline-block;
            vertical-align: middle;
            padding-right: 1.375rem;
            font-size: 1.375rem;
            color: $mainColorDarker;
        }
        ul {
            display: inline-block;
            li {
                display: inline-block;
                padding: 0 .4375rem;
                img {
                    vertical-align: middle;
                    
                }
            }
        }
    }
    
}
</style>

