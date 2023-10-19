<script>
  export default {
  
  }
</script>
<template>
  
  <header>
    <div class="top">
      <div class="container-sp d-flex justify-content-between py-2 align-items-center">
        <p class="my-1">We have a 95% Sucessful Pass Rate!</p>
        <div class="text">
          <i class="fa-solid fa-phone px-1"></i>
          <span>Give us a call to book your tuition! 1-800-555-555</span>
        </div>
      </div>
    </div>
    <div class="bottom">
      <div class="container-sp d-flex justify-content-between py-2">
    
        <div class="logo pt-1">
          <img src="/avada-drivers-logo-2x-200x39.png" alt="logo-avada-driving-school">
        </div>
        <nav class="mt-2">
          <ul>
           
            <li class="pb-1"><a href="#">Home</a></li>
            <li class="pb-1"><a href="#">About</a></li>
            <li class="pb-1"><a href="#">Prices</a></li>
            <li class="pb-1"><a href="#">Courses</a></li>
            <li class="pb-1"><a href="#">Locations</a></li>
            <li class="pb-1"><a href="#">Blog</a></li>
          </ul>
        </nav>
        
        <button>componente</button>
      </div>
    </div>
    
  </header>



</template>


<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

header {
  position: fixed;
  width: 100%;
  z-index: 999;

  .top {
    font-size: $sm-size;
    font-weight: 600;
    color: $dark-gray;
    background-color: $black;
  }
  .bottom {
    color: $white;
    background-color: rgba(10, 10, 10, 0.5);
    padding: 10px;
  }
  li{
    display: inline-block;
    margin: 0 25px;
    text-transform: uppercase;
    &:hover, &:active, &:focus {
      border-bottom: 1px solid $main-color;
      color: $main-color;
    }
    a {
    text-decoration: none;
    font-size: $nav-size;
    font-weight: 700;
    color: $white;
    &:active, &:focus, &:hover {
      color: $main-color;
    }
  }
  }

  }


.debug {
  border: 1px solid white;
}
</style>