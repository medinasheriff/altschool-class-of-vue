<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import { colorPicker } from "../composables/ColorPicker";

export default {
  setup() {
    const colors = ["green", "red", "blue", "purple"];
    const { message, matchColor } = colorPicker(colors);

    return { colors, message, matchColor };
  },
};
</script>

<style></style>
