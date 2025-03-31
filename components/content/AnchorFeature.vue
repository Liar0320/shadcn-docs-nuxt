<template>
  <FunctionAnchorFeature :source="{ anchor }" :tag="tag">
    <slot />
  </FunctionAnchorFeature>
</template>

<script setup lang="ts">
defineProps<{
  anchor: string;
  tag?: string;
}>();
</script>
