<script>
import Header from './components/Header/Header.vue';
import Main from './components/Main/Main.vue';
export default {
  name: 'app',
  components: {
    Header,
    Main
  }
}
</script>

<template>
  <Header />
  <Main />

</template>



<style lang="scss">

@use './scss/main.scss' as *;
@use "bootstrap/scss/bootstrap" as *;


</style>


<!-- TODO -->
<!--0. footer  -->
<!--1. Botton component -->
<!--2. dynamic nav + bedge-btn near courses -->
<!--3. socials -->
<!--4. hover to learn more buttons -->