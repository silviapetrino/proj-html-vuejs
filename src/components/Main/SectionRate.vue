<script>
import GenericCard from '../partials/GenericCard.vue';


export default {
  name: 'rate-section',
  components: {
    GenericCard

  }
}
</script>

<template>

<!-- this props (percentage, rate) are from component: Generic card!  -->

  <div class="container-sp">
    <div class="wrapper-cards d-flex gap-2">
      <GenericCard :percentage='95' :rate="'Pass Rate'"/>
      <GenericCard :percentage='100' :rate="'Referral Rate'"/>
      <GenericCard :percentage='0' :rate="'Accident Rate'"/>
    </div>
    
  </div>
 
</template>



<style lang="scss" scoped>

.container-sp {
  position: relative;
}
.wrapper-cards {
  position: absolute;
  top: -30px;
}

</style>