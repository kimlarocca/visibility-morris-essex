<template>
  <div class="p-5 bg-black rounded-lg logo">
    <NuxtLink to="/" class="plain clickable" aria-label="home">
      <p class="like-h3 text-white">{{ companyName }}</p>
    </NuxtLink>
  </div>
</template>

<style lang="scss" scoped>
.logo {
  p {
    margin-top: -5px;
  }
  &.minimal {
    padding: 0;
    background: transparent;
  }
}
</style>
