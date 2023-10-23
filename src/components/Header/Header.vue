<script>
  import CtaBtn from '../partials/buttons/CtaBtn.vue';
  import navsMenu from '../../data/navsMenu.js';
  export default {
    name: 'Header',
    components: {
      CtaBtn
    },
    data (){
      return {
        navsMenu
      }
    }
  }
</script>
<template>
  
  <header>
           <!-- header top  -->
    <div class="top">
      <div class="container-sp d-flex justify-content-between py-2 align-items-center">
        <p class="my-1">We have a 95% Sucessful Pass Rate!</p>
        <div class="text">
          <i class="fa-solid fa-phone px-1"></i>
          <span>Give us a call to book your tuition! 1-800-555-555</span>
        </div>
      </div>
    </div>
        <!-- /header top  -->
        <!-- header bottom  -->
    <div class="bottom">
      <div class="container-sp d-flex justify-content-between py-2">
    
        <div class="logo pt-1">
          <img src="/avada-drivers-logo-2x-200x39.png" alt="logo-avada-driving-school">
        </div>

        <nav class="mt-2">
          <ul>
            <li v-for="(item, index) in navsMenu.headerNavMenu" 
            :key="`head-${index}`" 
            class="pb-1">
            <a :href="item.href">{{ item.content }}</a>
            <span v-if="item.bedge" class="ms-1 badge bg-success">New</span>
            </li>
            <!-- cta button component  -->
            <CtaBtn :text="'book now'"/>
          </ul>
        </nav>

      </div>
    </div>
     <!-- /header bottom  -->
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
    font-weight: $fw-600;
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
    font-size: $main-size;
    font-weight: 700;
    color: $white;
    &:active, &:focus, &:hover {
      color: $main-color;
    }
  
  }
  }

  }
</style>