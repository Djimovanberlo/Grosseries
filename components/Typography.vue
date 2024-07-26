<template>
  <component :is="variant">
    <slot />
  </component>
</template>

<script setup lang="ts">
type Tag = "h1" | "h2" | "h3" | "h4" | "h5" | "h6" | "p" | "span";

interface TypographyProps {
  variant: Tag;
}

const { variant } = defineProps<TypographyProps>();
</script>

<style lang="less" scoped>
:is(h1, h2, h3, h4, h5, h6, p, span) {
  margin: 0;
}

h1 {
  font-size: 2rem;
}

h2 {
  font-size: 1.5rem;
}

h3 {
  font-size: 1.17rem;
}

h4 {
  font-size: 1rem;
}

h5 {
  font-size: 0.83rem;
}

h6 {
  font-size: 0.67rem;
}

p,
span {
  font-size: 1rem;
}
</style>
