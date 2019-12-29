<template>
  <div id="app">
    <Index />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Index from './components/Index.vue';

@Component({
  components: {
    Index,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
html {
  box-sizing: border-box;
  font-size: 62.5%; // 1rem = 16px;

  @include respond(small) {
    font-size: 50%; //1rem = 8px, 8/16 = 50%
  }
}

body {
  margin: 0;
  font-weight: 400;
  font-size: 16px;
  line-height: 1.7;
  font-family: $font-primary;
}
</style>
