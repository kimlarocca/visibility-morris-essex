<script setup>
const { isDarkMode } = useDarkMode()
const currentYear = new Date().getFullYear()
</script>

<template>
  <div class="container p-4">
    <Divider class="my-12" />
    <footer>
      <div class="grid lg:grid-cols-4 gap-16 mb-12">
        <div class="col-span-1 lg:col-span-2">
          <NuxtLink to="/" class="plain clickable" aria-label="home">
            <img
              v-if="isDarkMode"
              src="/images/visibility-brigade-logo-dark.png"
              alt="Morris Essex Visibility Brigade logo"
              class="visibility-brigade-logo mb-5"
            />
            <img
              v-else
              src="/images/visibility-brigade-logo.png"
              alt="Morris Essex Visibility Brigade logo"
              class="visibility-brigade-logo mb-5"
            />
            <Logo />
            <p class="mt-5">{{ tagLine }}</p>
          </NuxtLink>
        </div>
        <div>
          <p class="like-h4 mb-4">Quick Links</p>
          <ul class="space-y-2">
            <li v-for="link in navigationLinks" :key="link.label">
              <p>
                <NuxtLink :to="link.href + link.hash" :target="link.target">
                  {{ link.label }}
                </NuxtLink>
              </p>
            </li>
          </ul>
        </div>
        <div class="flex flex-col">
          <p class="like-h4 mb-5">Connect</p>
          <p class="mb-5">
            <i class="pi pi-envelope mr-2" />
            <a :href="`mailto:${emailAddress}`">
              {{ emailAddress }}
            </a>
          </p>
          <div class="flex space-x-4">
            <a
              v-for="social in socialLinks"
              :key="social.label"
              :href="social.url"
              :aria-label="social.label"
              class="icon-link plain clickable"
              :class="isDarkMode ? 'text-white' : 'text-black'"
            >
              <img
                v-if="social.icon === 'custom'"
                :src="social.iconSrc"
                :alt="social.label"
                class="custom"
                :class="{ 'filter invert': isDarkMode }"
              />
              <i v-else :class="social.icon" class="text-2xl"></i>
            </a>
          </div>
        </div>
      </div>
      <p class="small">
        Copyright © {{ currentYear }} {{ companyName }}. All Rights Reserved.
        <NuxtLink to="https://www.visibilitybrigade.com/privacy-policy" target="_blank">
          Privacy Policy
        </NuxtLink>
      </p>
    </footer>
  </div>
</template>

<style lang="scss">
footer {
  .visibility-brigade-logo {
    width: 220px;
  }
  .icon-link {
    display: flex;
    align-items: center;
  }
  .custom {
    max-width: 22px;
    width: 22px;
    height: 22px;
  }
}
</style>
