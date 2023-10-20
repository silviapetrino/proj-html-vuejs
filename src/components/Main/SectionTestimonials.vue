
<script>
import testimonialsCarousel from '../../data/testimonialsCarousel';

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
        ],
        testimonialsCarousel,
        currentIndex: 0
    }
  },
  methods: {
    nextSlide(index){
        this.currentIndex = index;
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

      <div v-for="(testimonial, index) in testimonialsCarousel" :key="`test${index}`" class="slide" :class="{ hide: index !== currentIndex }">
        <img :src="testimonial.photo" alt="sofia-photo" width="150">
        <p class="quote py-4">{{ testimonial.quote }}</p>
        <div class="name py-2">{{ testimonial.name }}</div>
      </div>
      
      <button @click="nextSlide(index)" v-for="(dot, index) in this.dots" :key="`dot${index}`" class="dot d-inline-block"></button>
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

  .hide {
    display: none;
  }

  .carousel-testimonials {
    .dot {
      width: 12px;
      height: 12px;
      margin: 5px;
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