<script>
import CtaBtn from './buttons/CtaBtn.vue';
export default {
  name: 'form',
  components: {
    CtaBtn
  }
}
</script>


<template>

  <div class="card d-flex flex-column text-align-center justify-content-center">
    <div class="text text-center py-3">
      <h3>First Lesson Free!</h3>
      <p>When you make a block booking with us your first lesson is included free.</p>
    </div>
    
    <form class="pb-4">
      <div class="form-group">
        <input type="text" class="form-control name" placeholder="Your Name*">
      </div>
      <div class="form-group">
        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Email*">
      </div>
      <div class="form-group">
        <input type="text" class="form-control" id="exampleInputPassword1" placeholder="Telephone">
      </div>
      <div class="form-group">
        <input type="text" class="form-control" id="exampleInputPassword1" placeholder="Location">
      </div>
      
      <CtaBtn :text="'request a callback'"/>
    </form>
</div>

 

</template>


<style lang="scss" scoped>

@use '../../scss/main.scss' as *;
.card {
  position: absolute;
  top: -80px;
  left: 50px;
  padding: 20px 35px;
  h3 {
  color: $main-color;
  font-weight: $fw-600;
  padding-bottom: 15px;
  }
  p:first-of-type {
    color: $dark-gray;
    font-size: $sm-size-b;
  }
  input {
    background-color: #F7F7F7;
    color: $dark-gray;
    margin: 20px 0;
    padding: 10px;
    font-size: $sm-size;
  }
  input.name {
    background-image: url('/image.png');
    background-repeat: no-repeat;
    background-position: 98%;
  }
  .cta {
    margin: 0 100px;
  }
 
}




</style>