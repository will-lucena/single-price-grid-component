<template>
  <div>
    <h1>{{ title }}</h1>
    <h2>{{ subTitle }}</h2>
    <h3>{{ description }}</h3>
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

<style></style>
