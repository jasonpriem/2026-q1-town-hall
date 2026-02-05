<template>
  <div class="slidev-layout title-layout">
    <div class="title-content">
      <slot />
    </div>
    <span class="page-number">{{ $slidev.nav.currentPage }}/{{ $slidev.nav.total }}</span>
    <img
      v-if="logo !== false"
      :src="logo || '/logo-white.png'"
      alt="OpenAlex"
      class="logo-corner"
    />
  </div>
</template>

<script setup>
defineProps({
  logo: {
    type: [String, Boolean],
    default: '/logo-white.png'
  }
})
</script>

<style scoped>
.title-layout {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  padding: var(--space-5) var(--space-6);
  position: relative;
}

.title-content {
  max-width: 900px;
}

.title-content :deep(h1) {
  font-size: 6.75rem;
  font-weight: 800;
  letter-spacing: -0.03em;
  line-height: 1.05;
  margin-bottom: var(--space-3);
}

.title-content :deep(p) {
  font-size: var(--text-lg);
  font-weight: 300;
  line-height: 1.4;
}

.title-content :deep(p.subtitle) {
  font-size: 0.8rem;
  font-weight: 400;
  margin-top: var(--space-2);
}

.title-content :deep(.title-logo) {
  height: 1.5rem;
  margin-bottom: 0.5rem;
}

.title-content :deep(.thin) {
  font-weight: 300;
}

.page-number {
  position: absolute;
  bottom: 1rem;
  left: 1.2rem;
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.75rem;
  color: var(--color-text);
  opacity: 0.2;
}

.logo-corner {
  position: absolute;
  bottom: 1rem;
  right: 1.2rem;
  height: 15px;
  opacity: 0.2;
}
</style>
