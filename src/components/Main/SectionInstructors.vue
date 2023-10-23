
<script>
import GenericCard from '../partials/GenericCard.vue';
import instructorsCards from '../../data/instructorsCards';
import CtaBtn from '../partials/buttons/CtaBtn.vue';

export default {
  name: 'Your-instructors-section',
  components: {
    GenericCard,
    CtaBtn
  },
  data(){
    return{
      instructorsCards
    }
  }
}
</script>


<template>

  <section id="instructors">

    <div class="container-sp d-flex">

      <div class="text-cta">
        <h2 class="py-3">your instructors</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro mollitia asperiores blanditiis quas iusto! Voluptatibus unde et modi accusantium error.</p>
      </div>
      <div class="box-btn"><CtaBtn :text="'more about us'"/></div>
    </div>

    <div id="instructors-names" class="container-sp d-flex justify-content-around">

      <GenericCard v-for="(instructor, index) in instructorsCards" :key="`instr-${index}`" :instructorCard="instructor"/>
     
    </div>

  </section>
 
 
</template>


<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

section#instructors{
  padding-top: 400px;


  #instructors-names {
    position: relative;
    top: 100px;
  }

  h2 {
    font-weight: $fw-600;
    color: $black;
    text-transform: capitalize;
  }
  p {
    color: $dark-gray;
    font-size: $main-size;
    width: 75%;
  }
  .cta {
    width: 350px;
  }
}

</style>