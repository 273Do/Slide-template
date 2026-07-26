<script setup lang="ts">
import { useNav } from "@slidev/client";

const slideTitle: string = ($slidev.configs.slideTitle ?? "").replaceAll("/", "");

const { currentSlideNo, total } = useNav();
</script>

<template>
  <footer class="flex items-center justify-between text-xs" text="[color:var(--muted-foreground)]">
    <span>{{ slideTitle }}</span>
    <span>{{ currentSlideNo }}/{{ total }}</span>
  </footer>
</template>
