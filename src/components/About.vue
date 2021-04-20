<template>
  <div>
    <h1>{{ title }}</h1>
    <p v-for="(advantage, index) in advantages" :key="index">
      {{ advantage }}
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
    advantages: {
      type: Array,
      default: undefined,
    },
  },
};
</script>

<style></style>
