<script>
import Form from '../partials/Form.vue';
  export default {
    name: 'main-form',
    components: {
      Form
    }
  }
</script>

<template>

<section id="form" class="py-4">
  <div class="container-sp d-flex">
    <div class="text w-50">
      <h2>Get Behind The Wheel</h2>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vel et iste nisi quibusdam aut. Consequatur repudiandae aliquam atque dolor architecto?</p>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa, dolorem? Dolore excepturi aliquid molestiae quae, obcaecati magnam adipisci ipsa consectetur architecto esse nam unde deserunt delectus labore aspernatur doloremque eius?</p>
    </div>
    <div class="form-box">
      <Form />
    </div>
    
  </div>
</section>
  


</template>


<style lang="scss" scoped>

@use '../../scss/main.scss' as *;


section#form .text {
  padding: 0 20px 0 0;
  position: relative;

  h2 {
    padding: 1.5rem 0;
    color: $black;
    font-weight: 600;
  }
  p {
    color: $dark-gray;
  }
  p:first-of-type {
    font-size: $main-size;
    line-height: 30px;
  }
  p:last-of-type{
    font-size: $size-13;
    line-height: 25px;
  }
}



</style>