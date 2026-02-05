<template>
  <div class="slidev-layout tiles-layout">
    <div class="tiles-inner">
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
.tiles-layout {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  height: 100%;
  padding: var(--space-5) var(--space-6);
  position: relative;
}

.tiles-inner {
  max-width: 100%;
}

.tiles-inner :deep(h1) {
  font-size: var(--text-2xl);
  font-weight: 800;
  letter-spacing: -0.02em;
  line-height: 1.15;
  padding-bottom: 0.75rem;
  margin-bottom: var(--space-4);
  position: relative;
}

.tiles-inner :deep(h1)::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: calc(-1 * var(--space-6));
  width: calc(100vw - 2 * var(--space-6));
  height: 1px;
  background: rgba(255, 255, 255, 0.1);
}

.tiles-inner :deep(ul) {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  list-style: none;
  padding: 0;
  margin: 0;
}

.tiles-inner :deep(li) {
  flex: 1 1 auto;
  min-width: 200px;
  max-width: 300px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  padding: 1.5rem 1.75rem;
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
}

.tiles-inner :deep(li) > strong:first-child,
.tiles-inner :deep(li) > p:first-child > strong:first-child {
  font-size: var(--text-xl);
  font-weight: 600;
  letter-spacing: -0.02em;
  display: block;
  line-height: 1.2;
}

.tiles-inner :deep(li) > em,
.tiles-inner :deep(li) > p > em {
  font-size: var(--text-base);
  font-weight: 400;
  font-style: normal;
  opacity: 0.5;
  display: block;
  margin-top: 0.15rem;
}

.tiles-inner :deep(p) {
  margin: 0;
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
