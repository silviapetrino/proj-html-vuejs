<script>
  import navsMenu from '../../data/navsMenu.js';
  import CtaBtn
   from '../partials/buttons/CtaBtn.vue';
  export default {
    name: 'Footer',
    components: {
      CtaBtn
    },
    data(){
      return {
        navsMenu
      }
    }
  }
</script>

<template>
  
  <footer>

    <div class="top">
      <div class="container-sp d-flex">
      <div class="col">
        <div class="logo pt-1">
          <img src="/avada-drivers-logo-2x-200x39.png" alt="logo-avada-driving-school" width="250">
        </div>
        <p class="py-2">Avada Driving School is the right choice for experienced drivers looking for a refresher course, or the brand new driver waiting to pass first time.</p>
      </div>
            <!-- contacts list  -->
      <div class="col text-center">
        <h4>contact details</h4>
        <nav class="contact text-start py-2">
          <ul class="fa-ul">
            <li class="py-2" v-for="(item, index) in navsMenu.footerContacts" :key="`contacts${index}`">
              <span class="fa-li"><i :class="item.icon"></i></span>
              <a class="pe-5" :href="item.href">{{ item.content }}</a>
            </li> 
          </ul>
        </nav>
      </div>
       <!-- courses list  -->
      <div class="col">
        <h4 class="text-center">courses</h4>
        <nav class="courses py-2">
          <ul class="fa-ul">
            <li class="py-2" v-for="(item, index) in navsMenu.footerCourses" :key="`courses${index}`">
              <span class="fa-li"><i :class="item.icon"></i></span>
              <a :href="item.href">{{ item.content }}</a>
            </li>
          </ul>
        </nav>
      </div>
      <!-- adv section with CtaBtn component  -->
      <div class="col text-center">
        <img src="/footer-ad-grid.png" alt="advertise" width="250" class="adv pb-4">
        <CtaBtn :text="'book now'"/>
      </div>
      </div>
    </div>

    <div class="bottom">
      <div class="container-sp">bottom</div>
    </div>

  </footer>
  
</template>


<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

footer {
  .container-sp {
    padding: 5rem 0;
  }
  .top {
  background-image: url('/footer-background-color.jpg');
  p {
    color: $dark-gray;
    font-size: $main-size;
    line-height: 30px;
  }
  h4 {
    color: $white;
    font-weight: $fw-600;
    text-transform: uppercase;
  }
  nav.contact {
    .fa-li  {
      color: $white;
    }
    a {
      color: $dark-gray;
      text-decoration: none;
    }
  }

  nav.courses {
    .fa-li, a {
      color: $main-color;
      font-size: $main-size-a;
    }
    a {
      text-decoration: none;
    }
  }

}
.debug {
  border: 1px solid white;
}
} 

</style>