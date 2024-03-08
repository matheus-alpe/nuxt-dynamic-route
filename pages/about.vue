<script lang="ts" setup>

</script>

<template>
  <div class="about-view">
    <h1>About view</h1>

    <nav>
      <NuxtLink to="/about">About</NuxtLink>
      <NuxtLink to="/about/test">Test</NuxtLink>
    </nav>

    <div class="inner-view">
      <NuxtPage />
    </div>
  </div>
</template>

<style>
.about-view {
  background: pink;
  border-radius: 5px;
  padding: .5rem;
  margin: 1rem 0;

  h1 {
    margin: 0;
  }

  nav {
    margin: 1rem 0;
  }

  .inner-view {
    background-color: rgba(3, 3, 3, .2);
    border-radius: 5px;
    padding: .5rem;
  }
}
</style>
