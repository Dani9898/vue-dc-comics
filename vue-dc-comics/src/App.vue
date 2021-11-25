<template>
  <div id="app">
    <Header/>
    <Jumbotron/>
    <ContenutoPrincipale/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import ContenutoPrincipale from './components/ContenutoPrincipale.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    ContenutoPrincipale,
    Footer
  }
}
</script>

<style lang="scss">

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background-color: #1c1c1c;
}
</style>
