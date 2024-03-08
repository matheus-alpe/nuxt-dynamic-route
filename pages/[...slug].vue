<template>
  <h1>
    Not found `{{
      Array.isArray($route.params.slug)
        ? $route.params.slug.join("/")
        : $route.params.slug
    }}` page
  </h1>

  <nav>
    <NuxtLink to="/">Home</NuxtLink>
  </nav>
</template>
