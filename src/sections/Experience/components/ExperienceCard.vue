<template>
  <div class="experience-card">
    <h3 class="experience-card__position">{{ title }}</h3>
    <a :href="companyWebsite" class="experience-card__company-name">{{
      companyName
    }}</a>
    <p class="experience-card__duration">{{ duration }}</p>
    <a :href="companyWebsite">
      <img
        :src="require(`@/assets/${companyLogoPath}`)"
        :alt="companyName + ' logo'"
        class="experience-card__company-logo"
      />
    </a>
    <p class="experience-card__description">
      {{ description }}
    </p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class EducationCard extends Vue {
  @Prop() title!: string;

  @Prop() companyName!: string;

  @Prop() companyWebsite!: string;

  @Prop() description!: string;

  @Prop() duration!: string;

  @Prop() companyLogoPath!: string;
}
</script>

<style scoped lang="scss">
.experience-card {
  position: relative;
  background-color: rgba(#fff, 0.7);
  border-radius: 20px;
  padding: 3rem 5rem;
  transition: all 0.2s;

  &:hover {
    transform: scale(1.02);
    box-shadow: 0.5rem 1rem 1.5rem rgba(black, 0.1);
  }

  &:not(:last-child) {
    margin-bottom: 3rem;
  }

  @include respond(medium) {
    padding: 2rem 3rem;
    border-radius: 15px;
  }

  &__position {
    color: $color-primary;
  }

  &__company-name {
    font-weight: 700;
    color: $color-secondary;
    text-decoration: none;
  }

  &__duration {
    margin-bottom: 10px;
  }

  &__company-logo {
    position: absolute;
    top: 4rem;
    right: 4rem;

    @include respond(medium) {
      display: none;
    }
  }
}
</style>
