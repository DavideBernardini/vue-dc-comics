<template>
        <header>
            <div class="container">
                <div class="logo">
                    <img src="../assets/img/dc-logo.png" alt="logo DC comics">
                </div>
                <nav>
                    <ul>
                        <li v-for="(link, index) in menu" :key="index"
                        :class="{active : link.current}">
                            <a href="#">{{link.text}}</a>
                        </li>
                    </ul>
                </nav>
            </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
        data() {
            return {
                menu: [
                    {
                        text: 'CHARACTERS',
                        current: false
                    },
                    {
                        text: 'COMICS',
                        current: 'true'
                    },
                    {
                        text: 'MOVIES',
                        current: false
                    },
                    {
                        text: 'TV',
                        current: false
                    },
                    {
                        text: 'GAMES',
                        current: false
                    },
                    {
                        text: 'COLLECTIBLES',
                        current: false
                    },
                    {
                        text: 'VIDEOS',
                        current: false
                    },
                    {
                        text: 'FANS',
                        current: false
                    },
                    {
                        text: 'NEWS',
                        current: false
                    },
                    {
                        text: 'SHOP',
                        current: false
                    }
                ]
            }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

header {
    height: 7.1875rem;
    .logo {
        display: inline-block;
        img {
            height: 5rem;
            
        }
    }
    nav {
        display: inline-block;
        ul {
            li {
                display: inline-block;
                margin: 0 1.25rem;
                height: 7.1875rem;
                line-height: 7.1875rem;
                &.active {
                    border-bottom: 5px solid $mainColor;
                    a {
                        color: $mainColor;
                    }
                }
            }
        }
    }
}
</style>
