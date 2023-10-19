
<script>
import LearnMoreBtn from './buttons/LearnMoreBtn.vue';
export default {
  name: 'learn-more',
  components: {
    LearnMoreBtn
  }
}
</script>

<template>

  <div class="box d-flex flex-column text-center align-items-center p-5">
    <img src="/public/courses-passplus-200x200.jpg" alt="courses-passpluss" width="180">
    <span class="d-inline-block py-2">Pass Plus</span>
    <LearnMoreBtn />
  </div>

</template>


<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

.box {
  color: $light-blue;
  span {
    font-size: $main-size-a;
    font-weight: $fw-700;
  }
}


</style>