<template>
    <main>
        <div class="jumbo titans"></div>
        <div class="comics">
            <div class="container">
                <h2>CURRENT SERIES</h2>
                <div class="comics_container">
                    <Comic v-for="(comic, index) in myJason" :key="index" :details="comic"/>
                </div>
                <button>LOAD MORE</button>
            </div>
        </div>
        <UsefullLinks/>
    </main>
</template>

<script>
import json from '../components/dc-comics.json';
import Comic from '../components/Comic';
import UsefullLinks from '../components/UsefullLinks';

export default {
    name: 'Main',
    components: {
        UsefullLinks,
        Comic
    },
    data() {
        return {
            myJason: json
        }
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";

.jumbo.titans {
    height: 25rem;
    background-image: url('../assets/img/jumbotron.jpg');
    background-size: cover;
}
.container {
    flex-direction: column;
    justify-content: center;
}
.comics {
    height: 42.5rem;
    background-color: #1c1c1c;
    color: #fff;
    .container {
        position: relative;
        h2 {
            font-size: 1.875rem;
            padding: .9375rem 1.875rem;
            background-color: $mainColor;
            position: absolute;
            top: 0;
            transform: translateY(-50%);
        }
    }
    &_container {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    button {
        display: block;
    }

}
</style>