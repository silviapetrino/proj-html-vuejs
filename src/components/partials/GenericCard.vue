<script>
import CircleRanges from './other-graphic-elements/CircleRanges.vue';


export default {
  name: 'generic-card',
  props: {
    percentage: Number,
    rate: String,
    instructorCard : Object,
  },
  components: {
    CircleRanges
  }
 
}
</script>

<template>
  

  <div class="wrapper-card">

    <div class="card-sp">

<!-- **************CARD WITH RANGE ********* -->
      <!-- Nb. se la percentuale è definita, la card generica inserisce il compontente cerchio con la relativa percentuale  -->
          <!-- the prop percentage is from component: CircleRanges!  -->
      <div v-if="percentage != null" class="circle py-5 d-flex flex-column justify-content-center align-items-center gap-5">
        <CircleRanges :percentage="percentage"/>
        <span class="rate py-1">{{ rate }}</span>
      </div>
      

<!-- **************CARD WITH ISTRUCTOR ********* -->
      <!-- Nb. se è presente l'array istructors, la card generica inserisce la i dati degli instructors importati nella Section Instructors  -->

      <div v-if="instructorCard" class="instructors d-flex flex-column justify-content-center align-items-center py-5">
        <img :src="instructorCard.photo" :alt="instructorCard.name" width="300">
        <h5 class="name pt-4">{{ instructorCard.name }}</h5>
        <!-- inserire componente social  -->
        <div>SOCIAL</div>
        <p class="description text-center">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ut, labore.</p>
      </div>

  

  </div>
    
  </div>


</template>



<style lang="scss" scoped>

@use '../../scss/main.scss' as *;

.card-sp{
  width: 370px;
  overflow: hidden;
  border-top: 5px solid $main-color;
  border-radius: 8px;
  box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.3);
  background-color: $white;
  cursor: pointer;
  transition: all .1s ease;
  &:hover {
    transform: scale(1.1);
  }

   // **************CARDS RATE ********* 
  span.rate {
    text-transform: uppercase;
    color: $dark-gray;
    font-weight: $fw-600;
  } 
  // **************CARDS ISTRUCTOR ********* 
  h5.name {
    color: $black;
    font-weight: $fw-600;
  }
  p.description {  
    color: $dark-gray;
    font-size: $sm-size-b;
    line-height: 25px;
    padding: 20px;
  }
 


 
}

 


</style>