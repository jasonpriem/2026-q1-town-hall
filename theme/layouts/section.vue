<template>
  <div class="slidev-layout section-layout">
    <div class="section-content">
      <slot />
    </div>
    <span class="page-number">{{ $slidev.nav.currentPage }}/{{ $slidev.nav.total }}</span>
    <img src="/logo-white.png" alt="OpenAlex" class="logo-corner" />
  </div>
</template>

<style scoped>
.section-layout {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  padding: var(--space-5) var(--space-6);
  position: relative;
}

.section-content {
  max-width: 800px;
}

.section-content :deep(h1) {
  font-size: var(--text-3xl);
  font-weight: 800;
  letter-spacing: -0.025em;
  line-height: 1.1;
  margin-bottom: var(--space-2);
}

.section-content :deep(p) {
  font-size: var(--text-base);
  font-weight: 300;
  line-height: 1.5;
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
