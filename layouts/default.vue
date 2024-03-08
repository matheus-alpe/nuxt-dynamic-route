<script lang="ts" setup>
const route = useRoute();
</script>

<template>
  <nav>
    <NuxtLink to="/">Home</NuxtLink>
    <NuxtLink to="/about">About</NuxtLink>
  </nav>

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
nav {
  display: grid;
  grid-auto-flow: column;
  grid-auto-columns: max-content;
  gap: .5rem;

  a {
    width: fit-content;
    padding: .5rem;
    border-radius: 5px;
    color: #000;
    background: rgba(3, 3, 3, .3);
    font-weight: bold;
    text-decoration: none;

    &.router-link-active {
      background: rgba(3, 3, 3, .5);
      color:#fcfcfc;
    }

    &.router-link-exact-active {
      background: rgba(3, 3, 3, .7);
      text-decoration: underline;
    }
  }
}

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
