<script>
import CircleRanges from './other-graphic-elements/CircleRanges.vue';

export default {
  name: 'generic-card',
  props: {
    percentage: Number,
    rate: String
  },
  components: {
    CircleRanges
  }
}
</script>

<template>
  

  <div class="wrapper-card">
    <div class="card-sp d-flex flex-column justify-content-center align-items-center gap-5 py-5">

      <!-- the prop percentage is from component: CircleRanges!  -->

      <CircleRanges :percentage="percentage"/>
    
      <span>{{ rate }}</span>
  

    </div>
  </div>



</template>



<style lang="scss" scoped>

@use '../../scss/main.scss' as *;

.card-sp{
  width: 370px;
  padding: 15px;
  overflow: hidden;
  border-top: 3px solid $main-color;
  border-radius: 5px;
  box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.3);
  background-color: $white;
  span {
    text-transform: uppercase;
    color: $dark-gray;
    font-weight: $fw-600;
  }
}

// ranges 


</style>