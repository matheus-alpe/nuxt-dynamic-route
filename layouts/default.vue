<script lang="ts" setup>
const route = useRoute();
</script>

<template>
  <slot />

  <ClientOnly>
    <div class="code">
      <p>name: <pre>{{ route.name }}</pre></p>
      <p>fullPath: <pre>{{ route.fullPath }}</pre></p>
      <p>params: <pre>{{ route.params }}</pre></p>
      <p>query: <pre>{{ route.query }}</pre></p>
      <p>meta: <pre>{{ route.meta }}</pre></p>
      <p>redirectedFrom: <pre>{{ route.redirectedFrom }}</pre></p>
    </div>
  </ClientOnly>
</template>

<style>
.code {
  background: rgba(3, 3, 3, .1);
  padding: 10px;
  width: fit-content;
  border-radius: 5px;

  p {
    display: flex;
    align-items: center;
    gap: .5rem;
    margin: .5rem 0;
  }

  pre {
    background: #333;
    border-radius: 5px;
    color: #fcfcfc;
    padding: .5rem;
    --size: .8rem;
    min-height: var(--size);
    font-size: var(--size);
    margin: 0;
  }
}
</style>
