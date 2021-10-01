<template>
  <div id="app">
    <Header/>
    <Hero :bgImage="require('./assets/img/jumbotron.jpg')"/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header';
import Hero from './components/Hero';
import Main from './components/Main';
import Footer from './components/Footer';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Hero
  }
}
</script>

<style lang="scss">
@import "./assets/style/common.scss";

#app {
  font-family: 'PT Sans Narrow', sans-serif;
}
</style>
