<script>

export default {
  name: 'main-jumbotron',
 
}
</script>


<template>

  <section id="jumbo">
    <div class="container-sp">
      <h1>Drive with Avada</h1>
      <p>We offer the finest driving tuition money can buy</p>
    </div>
    
  </section>

</template>


<style lang="scss" scoped>

@use '../../scss/main.scss' as *;

section#jumbo {
  background-image: url('/homepage-hero-background.jpg');
  background-size: 100%;
  background-repeat: no-repeat;
  color: $white;
  position: relative;
  .container-sp {
    padding: 290px 0 0 0;
  }
  h1 {
    font-weight: 600;
    letter-spacing: 1px;
  }
  p {
    padding: 0 0 130px 0;
  }
}


</style>