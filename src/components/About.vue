<template>
  <div class="card">
    <h1 class="title">{{ title }}</h1>
    <p v-for="(reason, index) in reasons" :key="index" class="reason">
      {{ reason }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: undefined,
    },
    reasons: {
      type: Array,
      default: undefined,
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/styles.scss";

.card {
  background-color: rgba($color: $primary, $alpha: 0.9);
}

.title {
  font-family: $font-family;
  color: #fff;
  margin-bottom: 1rem;
  font-size: 1.5rem;
}

.reason {
  font-family: $font-family;
  color: rgba($color: $grey, $alpha: 0.8);
  line-height: 1.5rem;
}
</style>
