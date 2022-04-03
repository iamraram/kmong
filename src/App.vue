<template>
  <div>
    <Header />
    <Mainimg />
    <Solve />
    <Tutor />
    <Videos />
    <Tuti />
    <Footer />
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Mainimg from './components/Mainimg.vue'
import Solve from './components/Solve.vue'
import Tutor from './components/Tutor.vue'
import Videos from './components/Videos.vue'
import Tuti from './components/Tuti.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Mainimg,
    Solve,
    Tutor,
    Videos,
    Tuti
  }
}
</script>

<style>

#app {
  width: 100%;
  height: auto;
  font-family: pretendard;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

</style>
