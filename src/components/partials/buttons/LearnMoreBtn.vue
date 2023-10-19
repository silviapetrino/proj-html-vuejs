<script>
export default {
  name: 'learn-more-btn'
}
</script>


<template>
  <div class="btn-sp">
    <button>learn more</button>
  </div>
     
</template>


<style lang="scss" scoped>
@use '../../../scss/main.scss' as *;

  button {
    color: $light-blue;
    font-weight: $fw-700;
    font-size: $sm-size-b;
    text-transform: uppercase;
    padding: 8px 18px;
    border: 3px solid $light-blue;
    border-radius: 25px;
  }

</style>