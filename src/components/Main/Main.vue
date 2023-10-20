<script>
import SectionJumbo from './SectionJumbo.vue';
import SectionForm from './SectionForm.vue';
import SectionStartCourses from './SectionStartCourses.vue';
import SectionRate from './SectionRate.vue';
import SectionInstructors from './SectionInstructors.vue';
import SectionTestimonials from './SectionTestimonials.vue';

export default {
  name: 'main',
  components: {
    SectionJumbo,
    SectionForm,
    SectionStartCourses,
    SectionRate,
    SectionInstructors,
    SectionTestimonials
  }
}
</script>

<template>
  
  <main>

    <SectionJumbo />
    <SectionForm />
    <SectionStartCourses />
    <SectionRate />
    <SectionInstructors />
    <SectionTestimonials />

  </main>


</template>

<style lang="scss" scoped>



</style>