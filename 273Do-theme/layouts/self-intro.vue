<script setup lang="ts">
import { resolveAssetUrl } from "../layoutHelper";

type Props = {
  image: string;
};

defineProps<Props>();
</script>

<template>
  <div class="slidev-layout flex flex-col h-full p-12">
    <slot name="title" />
    <div class="flex-1 flex gap-8 items-start mt-14">
      <img :src="resolveAssetUrl(image)" class="w-65 aspect-square shrink-0" />
      <div class="flex flex-col">
        <slot />
      </div>
    </div>
    <Footer />
  </div>
</template>
