
<script>
export default {
  name: 'Section-testimonials',
  data(){
    return {
      dots: [
        `<button class="dot"></button>`,
        `<button class="dot"></button>`,
        `<button class="dot"></button>`,
        `<button class="dot"></button>`,
        `<button class="dot"></button>`,
        ]
    }
  }
}
</script>

<template>


 <section id="testimonials" class="text-center">
  <div class="container-sp">
    <h2>testimonials</h2>
    <p>Here's what our drivers had to say about our services:</p>

    <div class="carousel-testimonials">
      <img src="/testimonial-sophia.png" alt="sofia-photo" width="150">
      <p class="quote py-4"><em>Lorem ipsum, dolor sit amet consectetur adipisicing elit.
        <br>Magni quam unde fuga voluptatibus dolores saepe culpa similique architecto? Assumenda, doloribus?</em></p>
      <div class="name py-2">Sofia Jones</div>
      <button v-for="(dot, index) in this.dots" :key="`dot${index}`" class="dot d-inline-block"></button>
    </div>
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
  p, .name {
    color: $dark-gray;
    font-size: 18px;
    line-height: 25px;
  }
  .name {
    font-weight: $fw-600;
  }

  .carousel-testimonials {
    .dot {
      width: 12px;
      height: 12px;
      margin: 3px;
      border-radius: 50%;
      border: 1px solid $dark-gray;
      cursor: pointer;
      
      &:focus {
      background-color: $dark-gray;
      }
    }
  }
  
}


</style>