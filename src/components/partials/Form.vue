<script>
export default {
  name: 'form'
}
</script>


<template>

  <div class="card">
    <div class="text text-center py-3">
      <h3>First Lesson Free!</h3>
      <p>When you make a block booking with us your first lesson is included free.</p>
    </div>
    
    <form>
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
       <!-- inserire componente bottone  -->
      <!-- <button type="submit" class="btn btn-primary">Submit</button> -->
    </form>
</div>

 

</template>


<style lang="scss" scoped>

@use '../../scss/main.scss' as *;
.card {
  border: 0px !important;
  position: absolute;
  top: -80px;
  left: 50px;
  padding: 20px 35px;
  box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.1);
  h3 {
  color: $main-color;
  font-weight: $fw-600;
  padding-bottom: 15px;
  }
  p:first-of-type {
    color: $dark-gray;
    font-size: $size-13;
  }
  input {
    background-color: #F7F7F7;
    margin: 20px 0;
    padding: 10px;
    font-size: $sm-size;
  }
  input.name {
    background-image: url('/image.png');
    background-repeat: no-repeat;
    background-position: 98%;
  }
}




</style>