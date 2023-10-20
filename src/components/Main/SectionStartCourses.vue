<script>
import CoursesInfo from '../partials/CoursesInfo.vue';
import LearnMore from '../partials/LearnMore.vue';
import cardsCourses from '../../data/cardsCourses';

export default {
  name: 'start-courses',
  data(){
    return{
      cardsCourses
    }
  },
  components: {
    CoursesInfo,
    LearnMore
  }
}
</script>

<template>
  
  <section id="start-courses">
        <!-- top section with call to action  -->
    <div class="top">
      <div class="container-sp d-flex justify-content-between align-items-center">
        <div class="text">
          <h2>Start Learning to Drive Today</h2>
          <p>Give us a call to schedule your first driving lesson</p>
        </div>
        <div class="call">
          <i class="fa-solid fa-phone mx-4"></i>
          <span>1-800-555-555</span>
        </div>
      </div>
    </div>

    <!-- inside, there are the CoursesInfo card component and the learn more cards -->
    <div class="bottom">
      <div class="container-sp d-flex">

        <CoursesInfo />

        <LearnMore v-for="(item, index) in cardsCourses" :key="`item${index}`" :cardObj="item"/>
     
      </div>
    </div>

    <svg class="fusion-big-triangle-candy" xmlns="http://www.w3.org/2000/svg" version="1.1" width="100%" height="100" viewBox="0 0 100 100" preserveAspectRatio="none" style="fill:#e4eaed;padding:0;"><path d="M-1 -1 L50 99 L101 -1 Z"></path></svg>


  </section>


</template>


<style lang="scss" scoped>

@use '../../scss/main.scss' as *;

section#start-courses {
  
  .top {
    background-image: url('/horizontal-cta-background.jpg');
    background-position: center;
    background-size: cover;
    padding: 80px;
    color: $white;
    h2, p {
    font-weight: $fw-600;
    }
    p {
    font-size: $main-size;
    }
    .call {
    font-size: $main-size-b;
    i {
      transform: rotate(260deg);
    }
  }
  }

  .bottom {
    background-image: url('/promise-background.jpg');
    background-size: cover;
    background-position-y: bottom;
    background-repeat: no-repeat;
    position: relative;
  }

}



</style>