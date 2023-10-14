<template>
  <button class="button">
    {{ buttonName }}
  </button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "AboutPage",
  props: {
    buttonName: {
      type: String,
      default: "Click me!",
    },
  },
});
</script>

<style lang="scss">
.button {
  background-color: #4caf50;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: block;
  font-size: 16px;
  cursor: pointer;
}
</style>
