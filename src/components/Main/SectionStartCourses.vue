<script>
export default {
  name: 'start-courses'
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
          <i class="fa-solid fa-phone px-1"></i>
          <span>1-800-555-555</span>
        </div>
      </div>
    </div>

    <div class="bottom">
      <div class="container-sp"></div>
    </div>

  </section>



</template>


<style lang="scss" scoped>

@use '../../scss/main.scss' as *;

section#start-courses .top {
  background-image: url('/public/horizontal-cta-background.jpg');
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
    font-size: $size-25;
  }
}

.debug {
  border: 1px solid black;
}
</style>