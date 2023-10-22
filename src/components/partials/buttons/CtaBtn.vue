<script>
export default {
  name: 'cta-btn',
  props: {
    text: String
  }
}
</script>


<template>

  <button class="cta">{{ text }}</button>
  
</template>


<style lang="scss" scoped>
@use '../../../scss/main.scss' as *;

button.cta {
  background-color: $main-color;
  color: $white;
  border: 0px;
  padding: 8px 25px;
  border-radius: 25px;
  text-transform: uppercase;
  font-weight: $fw-700;
  &:hover{
    background-color: darken($color: $main-color, $amount: 8);
  }
}

</style>