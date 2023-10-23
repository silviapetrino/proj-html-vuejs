<script>
import Header from './components/Header/Header.vue';
import Main from './components/Main/Main.vue';
import Footer from './components/Footer/Footer.vue';
export default {
  name: 'app',
  components: {
    Header,
    Main,
    Footer
  }
}
</script>

<template>
  
  <Header />
  <Main />
  <Footer />
  
</template>



<style lang="scss">

@use './scss/main.scss' as *;
@use "bootstrap/scss/bootstrap" as *;


</style>

