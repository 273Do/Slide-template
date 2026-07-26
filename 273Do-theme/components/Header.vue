<script setup lang="ts">
type Props = {
  date: number;
};

const { date } = defineProps<Props>();
</script>

<template>
  <footer class="flex items-center justify-between text-xs">
    <span>{{ date }}</span>
  </footer>
</template>
