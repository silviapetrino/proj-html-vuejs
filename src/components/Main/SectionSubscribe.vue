<script>
export default {
  name: 'subscribe'
}
</script>

<template>

  <section id="subscribe">
    <div class="container-sp text-center py-5 d-flex justify-content-center">
      <div class="col-8">
        <h3 class="py-3">Sign up to our Newsletter</h3>
        <input type="email" id="email">
           <!-- inserisci componente bottone  -->
        <p class="py-4">&#10098;We do not share your data with anybody, and only use its intended purpose&#10099;</p>
      </div> 
    </div>
 
  </section>

</template>


<style lang="scss" scoped>

@use '../../scss/main.scss' as *;

section#subscribe {
  background-image: url('/newsletter_background.jpg');
  background-size: contain;
  background-position: center;
  h3 {
    color: $black;
    font-weight: $fw-600;
  }
  p {
    color: $dark-gray;
  }
  input {
    width: 100%;
    border: 1px solid $dark-gray;
    border-radius: 3px;
    padding: 10px 0;
  }
}

</style>