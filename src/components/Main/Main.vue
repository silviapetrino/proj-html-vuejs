
<script>
import SectionJumbo from './SectionJumbo.vue';
import SectionForm from './SectionForm.vue';
import SectionStartCourses from './SectionStartCourses.vue';

export default {
  name: 'main',
  components: {
    SectionJumbo,
    SectionForm,
    SectionStartCourses
  }
}
</script>

<template>
  
  <main>

    <SectionJumbo />
    <SectionForm />
    <SectionStartCourses />

  </main>


</template>

<style lang="scss" scoped>



</style>