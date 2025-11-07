<script setup>
const visible = ref(false)
</script>

<template>
  <header class="rounded-lg">
    <div class="flex justify-between gap-4 items-center">
      <Logo />
      <i
        v-if="navigationLinks"
        class="bg-black p-4 rounded-full pi pi-bars text-xl text-white clickable"
        @click="visible = !visible"
        aria-label="Toggle navigation menu"
      />
      <Drawer v-model:visible="visible" position="right" class="bg-black border-0">
        <NuxtLink to="/" class="plain clickable" aria-label="home">
          <Logo class="minimal mb-8" />
        </NuxtLink>
        <p v-for="item in navigationLinks" class="mb-4">
          <NuxtLink
            :key="item.label"
            :to="item.href + item.hash"
            class="font-medium decoration-none text-white"
            @click="visible = false"
          >
            {{ item.label }}
          </NuxtLink>
        </p>
      </Drawer>
    </div>
  </header>
</template>

<style lang="scss">
header {
  position: absolute;
  z-index: 10;
  top: 1.5rem;
  left: 1.5rem;
  right: 1.5rem;
}
.p-drawer-header button {
  color: var(--p-button-primary-color) !important;
  background: var(--p-button-primary-background) !important;
  border: none !important;
  &:hover {
    background: var(--p-button-primary-hover-background) !important;
    color: var(--p-button-primary-hover-color) !important;
  }
  &:focus,
  &:focus-visible {
    outline-color: transparent !important;
    box-shadow: none !important;
  }
}
</style>
