<template>
  <div class="education-card">
    <h3 class="education-card__university-name">
      <a :href="schoolLink">{{ universityName }}</a>
    </h3>
    <p class="education-card__degree">{{ degree }}</p>
    <p class="education-card__honors">{{ honor }}</p>
    <p class="education-card__duration">{{ duration }}</p>
    <a :href="schoolLink">
      <img
        :src="require(`@/assets/${schoolLogoPath}`)"
        alt="Chulalongkorn University logo"
        class="education-card__university-logo"
      >
    </a>
    <ul class="education-card__description">
      <li v-for="description in descriptions" v-bind:key="description">
        {{ description }}
      </li>

    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class EducationCard extends Vue {
  @Prop() universityName!: string;

  @Prop() degree!: string;

  @Prop() honor!: string;

  @Prop() duration!: string;

  @Prop() schoolLogoPath!: string;

  @Prop() schoolLink!: string;

  @Prop() descriptions!: object;
}
</script>

<style scoped lang="scss">
.education-card {
  position: relative;
  background-color: rgba(#fff, .7);
  border-radius: 20px;
  padding: 3rem 5rem;
  transition: all .2s;

  &:hover {
    transform: scale(1.02);
    box-shadow: .5rem 1rem 1.5rem rgba(black, 0.1);
  }

  @include respond(medium) {
    padding: 2rem 3rem;
    border-radius: 15px;
  }

  &__position {
    color: $color-primary;
  }

  &__university-name {
    color: $color-primary;
    & > * {
      text-decoration: none;
      color: $color-primary;
    }
  }

  &__degree {
    font-weight: 700;
    color: $color-secondary;
  }

  &__honors {
    font-weight: 700;
    color: $color-grey-dark-2;
  }

  &__duration {
    margin-bottom: 10px;
  }

  &__university-logo {
    position: absolute;
    top: 3rem;
    right: 4rem;

    @include respond(medium) {
      display: none;
    }
  }

  &__description {
    margin-left: 3rem;

    @include respond(small) {
        margin-left: 2rem;
    }
  }
}
</style>
