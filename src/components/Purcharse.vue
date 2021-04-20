<template>
  <div>
    <h1>{{ title }}</h1>
    <div>
      <h2>
        <span>{{ formattedValue }}</span>
        <span>{{ frequency }}</span>
      </h2>
      <h2>{{ description }}</h2>
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

<style></style>
