<template>
  <div class="card">
    <h3 class="title">
      <a :href="link">{{ title }}</a>
    </h3>
    <div class="meta">{{ date }}</div>
    <p class="desc">{{ desc }}</p>
  </div>
</template>

<script setup>
defineProps(['title', 'date', 'desc', 'link'])
</script>

<style scoped>
.card {
  background: var(--vp-c-bg-soft);
  border-radius: 8px;
  padding: 1.5rem;
  margin-bottom: 1.2rem;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
  border: 1px solid var(--vp-c-border);
  transition: transform 0.2s, box-shadow 0.2s;
}
.card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}
.title {
  font-size: 1.2rem;
  margin-bottom: 0.4rem;
}
.title a {
  color: var(--vp-c-brand-1);
  text-decoration: none;
  font-weight: 600;
}
.title a:hover {
  color: var(--vp-c-brand-2);
  text-decoration: underline;
}
.meta {
  font-size: 0.85rem;
  color: var(--vp-c-text-2);
  margin-bottom: 0.6rem;
}
.desc {
  font-size: 0.95rem;
  color: var(--vp-c-text-1);
  line-height: 1.6;
}
</style>