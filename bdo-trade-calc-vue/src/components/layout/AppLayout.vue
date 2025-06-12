<script setup lang="ts">
import AppHeader from '@/components/layout/AppHeader.vue'
</script>

<template>
  <div class="app-layout dark-theme">
    <div class="card rounded-xl shadow-lg w-full max-w-5xl mx-auto p-6 md:p-8 space-y-8">
      <AppHeader />
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.app-layout {
  min-height: 100vh;
  padding: 1rem;
  background-color: #1a202c;
  color: #e2e8f0;
}

@media (min-width: 768px) {
  .app-layout {
    padding: 2rem;
  }
}

.card {
  background-color: #2d3748;
  border: 1px solid #4a5568;
  border-radius: 0.75rem;
  box-shadow:
    0 10px 15px -3px rgba(0, 0, 0, 0.1),
    0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.space-y-8 > * + * {
  margin-top: 2rem;
}

.rounded-xl {
  border-radius: 0.75rem;
}

.w-full {
  width: 100%;
}

.max-w-5xl {
  max-width: 64rem;
}

.mx-auto {
  margin-left: auto;
  margin-right: auto;
}

.p-6 {
  padding: 1.5rem;
}

@media (min-width: 768px) {
  .md\:p-8 {
    padding: 2rem;
  }
}
</style>
