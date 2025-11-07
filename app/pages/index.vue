<template>
  <div>
    <section class="hero inverse">
      <div class="p-6 h-full flex flex-col justify-between">
        <h1 class="like-h1 text-white mb-12" v-html="tagline" />
        <div class="mb-12">
          <p
            class="mb-6 text-xl sm:text-2xl font-semibold text-white"
            v-html="description"
          />
          <NuxtLink :to="ctaLink" class="plain">
            <Button :label="ctaText" class="white" />
          </NuxtLink>
        </div>
      </div>
    </section>

    <section class="about-us">
      <img src="/images/about-us.jpg" alt="About the Morris Essex Visibility Brigade" />
    </section>

    <section
      class="relative contrast rounded-xl mx-6 lg:mr-48 mt-8 lg:mt-16 mb-32"
      id="about-us"
    >
      <div class="p-8 sm:p-16 lg:p-24">
        <h2 class="like-h2 mb-8">About Us</h2>
        <p class="mb-6">
          The Morris Essex Visibility Brigade is a local group that creates awareness
          about our national crisis on overpasses and other public spaces in Morris and
          Essex County, NJ. Our goal is to remind neighbors of our nation's emergency, to
          protect democracy, and suggest simple actions they can take every day to resist.
        </p>
        <p>
          Our goal is to remind neighbors of our nation's emergency, to protect democracy,
          and suggest simple actions they can take every day to resist. We typically meet
          up on high-traffic pedestrian bridges during rush hour with pre-determined
          messages and stand over our messages, waving at passing cars. We take action and
          come together in community to make a difference and resist.
        </p>
      </div>
    </section>

    <section id="gallery" class="mb-40">
      <div
        class="elfsight-app-d78d4cd5-eb6b-4fcc-a63a-2f9efc2a2393"
        data-elfsight-app-lazy
      />
    </section>

    <section
      class="relative contrast rounded-xl mx-6 mt-8 lg:mt-16 mb-32"
      id="get-involved"
    >
      <div class="grid lg:grid-cols-3 gap-4">
        <div class="p-8 sm:p-16 lg:p-24 lg:col-span-2">
          <h2 class="like-h2 mb-8">Get Involved</h2>
          <h3 class="like-h3 mb-4">We Host Weekly Events!</h3>
          <p class="mb-4">
            We typically meet up on high-traffic pedestrian bridges during rush hour with
            pre-determined messages and stand over our messages, waving at passing cars.
            We take action and come together in community to make a difference and resist.
          </p>
          <p class="mb-8">
            Visit our
            <a :href="newMemberFormUrl" target="_blank" rel="nofollow noreferrer">
              new member request form</a
            >
            to get started. Together, we can make a difference!
          </p>
          <NuxtLink :to="ctaLink" class="plain">
            <Button :label="ctaText" class="white" />
          </NuxtLink>
        </div>
        <div>
          <NuxtLink
            :to="newMemberFormUrl"
            target="_blank"
            rel="nofollow noreferrer"
            class="plain"
          >
            <img
              src="/images/join-the-visibility-brigade.jpg"
              alt="Join the Morris Essex Visibility Brigade"
              class="rounded-xl w-full lg:w-fit lg:-mt-8"
            />
          </NuxtLink>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
onMounted(() => {
  const observer = new MutationObserver(() => {
    const element = document.querySelector('a[title="Free Instagram Feed widget"]')
    if (element) {
      element.remove()
      observer.disconnect()
    }
  })

  observer.observe(document.body, {
    childList: true,
    subtree: true,
  })
})
</script>

<style lang="scss">
@tailwind base;
.hero {
  background: url("/images/hero.jpg") no-repeat center center;
  background-size: cover;
  height: 100vh;
  min-height: fit-content;
  p {
    max-width: 800px;
  }
}

.about-us {
  width: 100%;
  text-align: right;
  margin-top: 2rem;
  @screen lg {
    margin-top: -8rem;
  }
  img {
    width: 70%;
    margin: 0 2rem 0 auto;
    @screen lg {
      width: auto;
      max-height: 20rem;
      margin: 0 4rem 0 auto;
    }
  }
}

// instagram feed overrides
.eapps-instagram-feed-posts-item {
  // border-radius: 12px;
}
.es-widget button {
  background: black !important;
  border-radius: 24px !important;
  padding: 0 2rem !important;
  text-transform: uppercase !important;
  font-weight: 500 !important;
  color: white !important;
  font-size: 1.25rem !important;
  height: 48px !important;
  line-height: 48px !important;
  width: fit-content !important;
  opacity: 1 !important;
  transition: var(--transition) !important;
  &:hover {
    opacity: var(--opacity-on-hover) !important;
  }
}
</style>
