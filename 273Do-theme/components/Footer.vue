<script setup lang="ts">
import { useNav } from "@slidev/client";

const { currentSlideNo, total } = useNav();
</script>

<template>
  <footer class="flex items-center justify-between text-xs" text="[color:var(--muted-foreground)]">
    <span>スライド名</span>
    <span>{{ currentSlideNo }}/{{ total }}</span>
  </footer>
</template>
