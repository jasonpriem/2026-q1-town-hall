<template>
  <div class="slidev-layout diagram-layout">
    <header class="diagram-header" v-if="$slots.header">
      <slot name="header" />
    </header>
    <div class="diagram-content">
      <slot />
    </div>
    <div class="header-line"></div>
    <span class="page-number">{{ $slidev.nav.currentPage }}/{{ $slidev.nav.total }}</span>
    <img src="/logo-white.png" alt="OpenAlex" class="logo-corner" />
  </div>
</template>

<style scoped>
.diagram-layout {
  display: flex;
  flex-direction: column;
  height: 100%;
  padding: var(--space-5) var(--space-6);
  position: relative;
}

.diagram-header {
  flex-shrink: 0;
  padding-bottom: 0.75rem;
  margin-bottom: var(--space-3);
}

.header-line {
  position: absolute;
  top: calc(var(--space-5) + 2.5rem + 1.125rem);
  left: var(--space-6);
  right: var(--space-6);
  height: 1px;
  background: rgba(255, 255, 255, 0.1);
}

.diagram-header :deep(h1) {
  font-size: var(--text-2xl);
  font-weight: 800;
  letter-spacing: -0.02em;
}

.diagram-header :deep(p) {
  font-size: var(--text-sm);
  font-weight: 300;
  margin-top: var(--space-1);
}

.diagram-content {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 0;
}

.diagram-content :deep(img) {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

.diagram-content :deep(p) {
  font-size: var(--text-sm);
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
