<template>
  <div class="skill-card">
    <img
      :src="require(`@/assets/${iconPath}`)"
      :alt="name + ' icon'"
      class=""
    />
    <p>{{ name }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class SkillCard extends Vue {
  @Prop() iconPath!: string;

  @Prop() name!: string;
}
</script>

<style scoped lang="scss">
.skill-card {
  width: 21%;
  margin-bottom: 3rem;

  @include respond(small) {
    width: 34%;
  }

  img {
    width: 75px;
    height: auto;
    border-radius: 15%;
    margin-bottom: 1rem;
    background-color: #fff;
  }

  p {
    text-align: center;
    line-height: 1.4;
  }
}
</style>
