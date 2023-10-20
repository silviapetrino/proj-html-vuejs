<script>
export default {
  name: 'circle-ranges',
  props: {
   percentage: Number
  }
}
</script>

<template>
  
  <div class="progress-circle over50 p100">
   <span>{{ percentage }} %</span>
   <div v-if="percentage === 100" class="left-half-clipper">
      <div class="first50-bar"></div>
      <div class="value-bar"></div>
   </div>
   <div v-if="percentage === 95" class="progress-circle over50 p95">
   <span>{{ percentage }} %</span>
   <div class="left-half-clipper">
      <div class="first50-bar"></div>
      <div class="value-bar"></div>
   </div>
   </div>
  </div>



</template>


<style lang="scss" scoped>

@use '../../../scss/main.scss' as *;
.progress-circle {
   font-size: 40px;
  //  margin: 10px;
   position: relative; /* so that children can be absolutely positioned */
   padding: 0;
   width: 5em;
   height: 5em;
   background-color: #F2E9E1; 
   border-radius: 50%;
   line-height: 5em;
}

.progress-circle:after{
    border: none;
    position: absolute;
    top: 0.35em;
    left: 0.35em;
    text-align: center;
    display: block;
    border-radius: 50%;
    width: 4.3em;
    height: 4.3em;
    background-color: white;
    content: " ";
}
/* Text inside the control */
.progress-circle span {
    position: absolute;
    line-height: 5em;
    width: 5em;
    text-align: center;
    display: block;
    color: $dark-gray;
    z-index: 2;
}
.left-half-clipper { 
   /* a round circle */
   border-radius: 50%;
   width: 5em;
   height: 5em;
   position: absolute; /* needed for clipping */
   clip: rect(0, 5em, 5em, 2.5em); /* clips the whole left half*/ 
}
/* when p>50, don't clip left half*/
.progress-circle.over50 .left-half-clipper {
   clip: rect(auto,auto,auto,auto);
}
.value-bar {
   /*This is an overlayed square, that is made round with the border radius,
   then it is cut to display only the left half, then rotated clockwise
   to escape the outer clipping path.*/ 
   position: absolute; /*needed for clipping*/
   clip: rect(0, 2.5em, 5em, 0);
   width: 5em;
   height: 5em;
   border-radius: 50%;
   border: 0.45em solid $main-color; /*The border is 0.35 but making it larger removes visual artifacts */
   /*background-color: #4D642D;*/ /* for debug */
   box-sizing: border-box;
  
}

/* Progress bar filling the whole right half for values above 50% */
.progress-circle.over50 .first50-bar {
   /*Progress bar for the first 50%, filling the whole right half*/
   position: absolute; /*needed for clipping*/
   clip: rect(0, 5em, 5em, 2.5em);
   background-color: $main-color;
   border-radius: 50%;
   width: 5em;
   height: 5em;
}
.progress-circle.p95 .value-bar { transform: rotate(340deg); }

</style>