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
import SectionHome from './sections/Home/Home.vue';
import SectionAboutMe from './sections/AboutMe/AboutMe.vue';
import SectionSkill from './sections/Skill/Skill.vue';
import SectionExperience from './sections/Experience/Experience.vue';
import SectionProject from './sections/Project/Project.vue';
import SectionEducation from './sections/Education/Education.vue';

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
