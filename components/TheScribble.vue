<script setup lang="ts">
import { defineAsyncComponent } from 'vue';

interface Props {
  name: string;
}

const props = defineProps<Props>();

// Dynamically import SVG based on the name prop
const ScribbleSvg = defineAsyncComponent(() =>
  import(`../styles/assets/scribbels/${props.name}.svg`),
);
</script>

<template>
  <ScribbleSvg />
</template>
