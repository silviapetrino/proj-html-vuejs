
<script>
export default {
  name: 'Section-testimonials'
}
</script>

<template>


 <section id="testimonials" class="text-center">
  <div class="container-sp">
    <h2>testimonials</h2>
    <p>Here's what our drivers had to say about our services:</p>
   
  </div>
 </section>

  
</template>


<style lang="scss" scoped>

@use '../../scss/main.scss' as *;


section#testimonials {
  background-image: url('/testimonial-background.jpg') ;
  background-position: center;
  background-size: cover;
  padding: 200px;


  h2 {
    font-weight: $fw-600;
    color: $black;
    text-transform: capitalize;
  }
  p {
    color: $dark-gray;
    font-size: $main-size;
  }
}


</style>