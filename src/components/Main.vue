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
    height: 43.125rem;
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
            left: 0;
            transform: translateY(-50%);
        }
    }
    &_container {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
    }
    button {
        margin-top: 2.8125rem;
        padding: .625rem 3.75rem;
        border-radius: 0;
        border: none;
        font-weight: bold;
        color: #fff;
        background-color: $mainColor;
        font-size: 1rem;
    }


}
</style>