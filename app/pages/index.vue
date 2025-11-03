<template>
  <div>
    <section class="hero flex flex-col items-center justify-center mb-12">
      <div class="container p-4">
        <h1 class="visibility-brigade">
          <span>r</span>
          <span>u</span>
          <span>s</span>
          <span>h</span>
          <span class="spacer" />
          <span>h</span>
          <span>o</span>
          <span>u</span>
          <span>r</span>
          <span class="spacer" />
          <span>r</span>
          <span>e</span>
          <span>s</span>
          <span>i</span>
          <span>s</span>
          <span>t</span>
          <span>a</span>
          <span>n</span>
          <span>c</span>
          <span>e</span>
        </h1>
        <p class="my-9 text-xl font-medium text-white">
          {{ tagLine }}
        </p>
        <NuxtLink :to="heroCtaLink" class="mr-3">
          <Button :label="heroCtaText" />
        </NuxtLink>
      </div>
    </section>
    <section class="container p-4">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor
        incididunt ut labore et dolore magna aliqua.
      </p>
    </section>
  </div>
</template>

<style lang="scss" scoped>
.hero {
  background: url("/images/hero.jpg") no-repeat center center;
  background-size: cover;
  min-height: 600px;
}
</style>
