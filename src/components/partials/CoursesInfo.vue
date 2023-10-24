<script>
import CtaBtn from './buttons/CtaBtn.vue';
export default {
  name: 'card-courses-info',
  components: {
    CtaBtn
  }
}
</script>


<template>

  <div class="wrapper-card">
    <div id="courses-info" class="card">
    <img src="/new-corner.jpg" alt="new" width="100">
    <div class="text text-center py-3">
      <h2>Courses</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nisi minima cumque magni sequi aspernatur laborum, dolor perferendis? Ipsa ex perferendis, voluptatibus nostrum error ab esse</p>
    </div>
    <CtaBtn :text="'course information'" />
  </div>

    

   
</div>

</template>



<style lang="scss" scoped>

@use '../../scss/main.scss' as *;

.card{
  width: 400px;
  padding: 30px 20px 50px 20px;
  position: relative;
  top: -20px;
  overflow: hidden;
  img {
    position: absolute;
    top: 0;
    left: 0;
  }
  h2 {
    font-weight: $fw-600;
    color: $black;
    padding: 1rem;
  }
  p {
    color: $dark-gray;
    font-size: $sm-size-b;
    line-height: 25px;
    padding: 20px;
  }
  .cta {
    margin: 0 60px;
  }
}

</style>