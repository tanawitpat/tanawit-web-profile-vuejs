<template>
  <div class="cards__card">
    <h3 class="cards__card--topic">{{ categoryName }}</h3>
    <div class="cards__card--content">
      <SkillCard
        v-for="skill in skills"
        :key="skill.name"
        :name="skill.name"
        :iconPath="skill.iconPath"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import SkillCard from './SkillCard.vue';

const SkillCategoryProps = Vue.extend({
  props: {
    categoryName: String,
    skills: Object,
  },
});

@Component({
  components: {
    SkillCard,
  },
})
export default class SkillCategory extends SkillCategoryProps {}
</script>

<style scoped lang="scss">
.cards {
  color: #fff;
  max-width: 120rem;
  margin: 0 auto;

  display: grid;
  grid-template-columns: repeat(2, 1fr);

  @include respond(largest) {
    grid-template-columns: 1fr;
  }

  &__card {
    text-align: center;

    &:not(:last-child) {
      margin-bottom: 3rem;
    }

    &--topic {
      text-align: center;
      margin-bottom: 3rem;
    }

    &--content {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
    }
  }
}
</style>
