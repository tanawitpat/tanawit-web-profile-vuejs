<template>
  <div id="index">
    <SectionHome />
    <SectionAboutMe />
    <SectionSkill />
    <SectionExperience />
    <SectionProject />
    <SectionEducation />
  </div>
</template>

<script lang="ts">
import SectionHome from './sections/Home.vue';
import SectionAboutMe from './sections/AboutMe.vue';
import SectionSkill from './sections/Skill.vue';
import SectionExperience from './sections/Experience.vue';
import SectionProject from './sections/Project.vue';
import SectionEducation from './sections/Education.vue';

export default {
  name: 'index',
  components: {
    SectionHome,
    SectionAboutMe,
    SectionSkill,
    SectionExperience,
    SectionProject,
    SectionEducation,
  },
};
</script>
