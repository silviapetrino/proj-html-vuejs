
<script>
import SectionJumbo from './SectionJumbo.vue';
import SectionForm from './SectionForm.vue';
import SectionStartCourses from './SectionStartCourses.vue';
import SectionRate from './SectionRate.vue';
import SectionInstructors from './SectionInstructors.vue';

export default {
  name: 'main',
  components: {
    SectionJumbo,
    SectionForm,
    SectionStartCourses,
    SectionRate,
    SectionInstructors
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

  </main>


</template>

<style lang="scss" scoped>



</style>