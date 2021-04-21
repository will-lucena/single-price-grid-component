<template>
  <div class="card">
    <h1 class="title">{{ title }}</h1>
    <div>
      <h2 class="subTitle">
        <span>{{ formattedValue }}</span>
        <span class="subTitle--frequency">{{ frequency }}</span>
      </h2>
      <h2 class="description">{{ description }}</h2>
    </div>
    <custom-button :text="callToAction" />
  </div>
</template>

<script>
import CustomButton from "./CustomButton.vue";

export default {
  components: { CustomButton },
  props: {
    title: {
      type: String,
      default: undefined,
    },
    value: {
      type: Number,
      default: undefined,
    },
    frequency: {
      type: String,
      default: undefined,
    },
    description: {
      type: String,
      default: undefined,
    },
  },
  data() {
    return {
      callToAction: "Sign Up",
    };
  },
  computed: {
    formattedValue() {
      return `$${this.value}`;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/styles.scss";

.card {
  background-color: #2ab2af;
}

.title {
  font-family: $font-family;
  color: #fff;
  font-size: 1.5rem;
}

.subTitle {
  font-family: $font-family;
  color: #fff;
  font-size: 2rem;
  margin: 1rem 0 0.5rem;
}

.subTitle--frequency {
  color: rgba($color: $grey, $alpha: 0.3);
  margin-left: 0.6rem;
  font-size: 1rem;
  font-weight: 400;
}

.description {
  font-family: $font-family;
  font-weight: 400;
  color: rgba($color: $grey, $alpha: 0.7);
  font-size: 1rem;
  margin-bottom: 2rem;
}
</style>
