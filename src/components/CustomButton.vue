<template>
  <button class="button">{{ text }}</button>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: undefined,
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/styles.scss";
.button {
  background-color: $secondary;
  border: none;
  padding: 1rem;
  border-radius: 0.3rem;
  font-family: $font-family;
  color: #fff;
  font-size: 1rem;
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);

  cursor: pointer;
  outline: none;
}

.button:focus {
  background-color: rgba($color: $secondary, $alpha: 0.8);
  border: none;
}

.button:hover {
  transition: linear 0.2s;
  background-color: rgba($color: $secondary, $alpha: 0.8);
}
</style>
