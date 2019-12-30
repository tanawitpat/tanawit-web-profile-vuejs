<template>
  <div id="index">
    <SectionHome />
    <SectionAboutMe />
  </div>
</template>

<script lang="ts">
import SectionHome from './sections/Home.vue';
import SectionAboutMe from './sections/AboutMe.vue';

export default {
  name: 'index',
  components: {
    SectionHome,
    SectionAboutMe,
  },
};
</script>
