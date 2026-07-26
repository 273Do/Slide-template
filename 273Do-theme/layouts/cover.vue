<script setup lang="ts">
const { slideTitle, eventTitle, eventSubTitle } = $slidev.configs;

const slideTitleSplit: string[] = (slideTitle ?? "").split("/");
</script>

<template>
  <div class="slidev-layout flex flex-col h-full p-12">
    <Header />
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
          <span>{{ eventTitle }}</span>
          <span>{{ eventSubTitle }}</span>
        </div>
        <img src="/imgs/273do-logo.svg" class="w-20 mt-4" />
      </div>
    </div>
  </div>
</template>
