<template>
  <div class="hello">
    <SectionHome />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import SectionHome from './sections/Home.vue';

@Component({
  components: {
    SectionHome,
  },
})
export default class App extends Vue {}
</script>
