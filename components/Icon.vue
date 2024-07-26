<template>
  <component :is="iconName" />
</template>

<script setup lang="ts">
interface IconProps {
  iconName: "chevron-up" | "chevron-down" | "xmark" | "arrow-right";
}

const { iconName } = defineProps<IconProps>();
</script>
