<template>
  <div class="card">
    <h1 class="title">{{ title }}</h1>
    <h2 class="subTitle">{{ subTitle }}</h2>
    <h3 class="description">{{ description }}</h3>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: undefined,
    },
    subTitle: {
      type: String,
      default: undefined,
    },
    description: {
      type: String,
      default: undefined,
    },
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/styles.scss";

.card {
  background-color: #fff;
}

.title {
  font-family: $font-family;
  color: $primary;
  font-size: 1.5rem;
}

.subTitle {
  font-family: $font-family;
  color: $secondary;
  font-size: 1rem;
  margin: 1.5rem 0;
}

.description {
  font-family: $font-family;
  color: rgba($color: $primary-darker, $alpha: 0.6);
  font-size: 1rem;
}
</style>
