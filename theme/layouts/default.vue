<template>
  <div class="slidev-layout default-layout">
    <slot />
    <div class="header-line"></div>
    <span class="page-number">{{ $slidev.nav.currentPage }}/{{ $slidev.nav.total }}</span>
    <img src="/logo-white.png" alt="OpenAlex" class="logo-corner" />
  </div>
</template>

<style scoped>
.default-layout {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  padding: var(--space-5) var(--space-6);
  height: 100%;
  position: relative;
}

.default-layout :deep(h1) {
  font-size: var(--text-2xl);
  font-weight: 800;
  letter-spacing: -0.02em;
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

.default-layout :deep(p) {
  max-width: 800px;
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
