<template>
  <div class="body text-primary">
    <main>
      <AboutHeader />
      <!-- <JobDropdown v-if="dataStore.job" /> -->
      <ContactHero />
      <ContactMessage />
    </main>
    <AppFooter />
  </div>
</template>

<script setup lang="ts">
import { useDataStore } from '@/stores/data'

const dataStore = useDataStore();
</script>

<style scoped></style>
