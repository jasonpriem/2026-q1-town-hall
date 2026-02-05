<template>
  <div class="slidev-layout demo-layout">
    <div class="demo-content">
      <slot />
    </div>
    <div class="header-line"></div>
    <span class="page-number">{{ $slidev.nav.currentPage }}/{{ $slidev.nav.total }}</span>
    <img src="/logo-white.png" alt="OpenAlex" class="logo-corner" />
  </div>
</template>

<style scoped>
.demo-layout {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  height: 100%;
  padding: var(--space-5) var(--space-6);
  background: var(--color-bg);
  position: relative;
}

.demo-content {
  max-width: 800px;
}

.demo-content :deep(h1) {
  font-size: var(--text-2xl);
  font-weight: 800;
  letter-spacing: -0.02em;
  line-height: 1.15;
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

.demo-content :deep(p) {
  font-size: var(--text-base);
  font-weight: 300;
  margin-top: var(--space-2);
  line-height: 1.5;
}

.demo-content :deep(.prompt-box) {
  font-family: 'JetBrains Mono', monospace;
  font-size: 1.1rem;
  line-height: 1.7;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  padding: 1.25rem 1.5rem;
  margin-top: var(--space-3);
  color: rgba(255, 255, 255, 0.85);
}

.demo-content :deep(.prompt-box ul) {
  list-style: disc;
  padding-left: 1.5rem;
  margin: 0;
}

.demo-content :deep(.prompt-box li) {
  margin-bottom: 0.35rem;
  font-size: 1.1rem;
}

.demo-content :deep(.screenshot) {
  margin-top: var(--space-3);
  border-radius: 8px;
  max-height: 420px;
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
</style>
