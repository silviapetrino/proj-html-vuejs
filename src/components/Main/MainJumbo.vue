<script>
export default {
  name: 'main-jumbotron'
}
</script>


<template>

  <section id="main-jumbo">
    <div class="container-sp">
      <h1>Drive with Avada</h1>
      <p>We offer the finest driving tuition money can buy</p>
    </div>
  </section>

</template>


<style lang="scss" scoped>

@use '../../scss/main.scss' as *;

section#main-jumbo {
  background-image: url('/homepage-hero-background.jpg');
  background-size: 100%;
  background-repeat: no-repeat;
  padding: 290px;
  color: $white;
  h1 {
    font-weight: 600;
    letter-spacing: 1px;
  }
}

.debug {
  border: 1px solid white;
}

</style>