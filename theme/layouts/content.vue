<template>
  <div class="slidev-layout content-layout">
    <div class="content-inner">
      <span v-if="section" class="section-indicator">{{ section }}</span>
      <slot />
    </div>
    <span class="page-number">{{ $slidev.nav.currentPage }}/{{ $slidev.nav.total }}</span>
    <img src="/logo-white.png" alt="OpenAlex" class="logo-corner" />
  </div>
</template>

<script setup>
defineProps({
  section: {
    type: String,
    default: ''
  }
})
</script>

<style scoped>
.content-layout {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  height: 100%;
  padding: var(--space-5) var(--space-6);
  position: relative;
}

.content-inner {
  max-width: 900px;
}

.content-inner :deep(h1) {
  font-size: var(--text-2xl);
  font-weight: 800;
  letter-spacing: -0.02em;
  line-height: 1.15;
  padding-bottom: 0.75rem;
  margin-bottom: var(--space-3);
  position: relative;
}

.content-inner :deep(h1)::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: calc(-1 * var(--space-6));
  width: calc(100vw - 2 * var(--space-6));
  height: 1px;
  background: rgba(255, 255, 255, 0.1);
}

.content-inner :deep(h2) {
  font-size: var(--text-lg);
  font-weight: 800;
  letter-spacing: -0.01em;
  margin-bottom: var(--space-2);
  margin-top: var(--space-3);
}

.content-inner :deep(p) {
  font-size: var(--text-base);
  line-height: 1.5;
  margin-bottom: var(--space-2);
  max-width: 800px;
}

.content-inner :deep(ul),
.content-inner :deep(ol) {
  margin-top: var(--space-1);
}

.content-inner :deep(li) {
  margin-bottom: 0.35rem;
}

.content-inner :deep(.columns) {
  margin-top: var(--space-2);
}

.content-inner :deep(.screenshot) {
  margin-top: var(--space-3);
  border-radius: 8px;
  max-height: 380px;
  width: auto;
  box-shadow: 0 4px 24px rgba(0, 0, 0, 0.4);
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

.section-indicator {
  display: block;
  font-family: 'Inter', sans-serif;
  font-size: 0.75rem;
  font-weight: 400;
  color: var(--color-text);
  letter-spacing: 0.02em;
  margin-bottom: 0.5rem;
}
</style>
