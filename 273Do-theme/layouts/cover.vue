<script setup lang="ts">
import { resolveAssetUrl } from "../layoutHelper";

type Props = {
  date: number;
  slideTitle: string;
  logo: string;
};

const { slideTitle } = defineProps<Props>();

const slideTitleSplit: string[] = slideTitle.split("/");
</script>

<template>
  <div class="slidev-layout flex flex-col h-full p-12">
    <Header :date="date" />
    <div class="flex-1 flex flex-col justify-center">
      <span
        v-for="(word, index) in slideTitleSplit"
        :key="index"
        class="inline-block w-fit text-6xl leading-tight"
        bg="[var(--primary)]"
        text="[color:var(--primary-foreground)]"
        >{{ word }}</span
      >
      <div class="flex w-full items-center justify-between">
        <div class="flex flex-col mt-10">
          <slot name="eventTitle" />
        </div>
        <img :src="resolveAssetUrl(logo)" class="w-20 mt-12" />
      </div>
    </div>
    <slot />
  </div>
</template>
