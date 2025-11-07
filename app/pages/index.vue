<template>
  <div>
    <section class="hero">
      <div class="p-6 h-full flex flex-col justify-between">
        <h1 class="text-white mb-12">{{ tagline }}</h1>
        <div class="mb-12">
          <p class="mb-6 text-xl sm:text-2xl font-semibold text-white">
            {{ description }}
          </p>
          <NuxtLink :to="ctaLink" class="mr-3">
            <Button :label="ctaText" />
          </NuxtLink>
        </div>
      </div>
    </section>
    <section class="highlight p-32" id="get-involved">
      <div class="container grid lg:grid-cols-2 gap-16">
        <div>
          <a :href="newMemberFormUrl" target="_blank" rel="nofollow noreferrer">
            <img
              src="/images/join-the-visibility-brigade.jpg"
              alt="Join the Morris Essex Visibility Brigade"
              class="rounded-lg shadow-lg clickable"
            />
          </a>
        </div>
        <div>
          <h2 class="mb-8">About Us</h2>
          <p class="mb-6">
            The Morris Essex Visibility Brigade is a local group that creates awareness
            about our national crisis on overpasses and other public spaces in Morris and
            Essex County, NJ. Our goal is to remind neighbors of our nation's emergency,
            to protect democracy, and suggest simple actions they can take every day to
            resist.
          </p>
        </div>
      </div>
    </section>
    <section class="banner px-4 py-12 contrast flex items-center justify-center">
      <h2 class="visibility-brigade contrast text-center">
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
      </h2>
    </section>
    <section class="container p-6 py-32">
      <div
        class="elfsight-app-d78d4cd5-eb6b-4fcc-a63a-2f9efc2a2393"
        data-elfsight-app-lazy
      />
    </section>
    <section class="py-16" id="get-involved">
      <div class="container p-4">
        <h2 class="mb-8">Get Involved</h2>
        <p class="mb-4">
          Your worries about what is happening to our country are valid and real. Millions
          of people feel exactly as you do. The problem is that everyone is looking around
          and everything still feels normal, even when it is not. That's why we do what we
          do: to remind you that we are in trouble.
        </p>
        <p class="mb-8">
          The truth is, nonviolent action is the antidote for despair and the more that
          you do to help save our democracy, the better you will feel. Trust us on this
          last point. Now that you are awakened to this truth, learn what you can do right
          now.
        </p>

        <h3 class="mb-6">We Host Weekly Events!</h3>
        <p class="mb-4">
          We typically meet up on high-traffic pedestrian bridges during rush hour with
          pre-determined messages and stand over our messages, waving at passing cars. We
          take action and come together in community to make a difference and resist.
          Visit our
          <a :href="newMemberFormUrl" target="_blank" rel="nofollow noreferrer">
            new member request form
          </a>
          to get started. Together, we can make a difference!
        </p>

        <NuxtLink :to="ctaLink" class="mr-3">
          <Button :label="ctaText" />
        </NuxtLink>
      </div>
    </section>
  </div>
</template>

<style lang="scss">
.hero {
  background: url("/images/hero.jpg") no-repeat center center;
  background-size: cover;
  height: 100vh;
  min-height: fit-content;
  p {
    max-width: 800px;
  }
}
.eapps-instagram-feed-posts-item {
  // border-radius: 24px;
}
.es-widget [title="Free Instagram Feed widget"],
.es-widget a:not(.eapps-instagram-feed-posts-item-link) {
  display: none !important;
}
</style>
