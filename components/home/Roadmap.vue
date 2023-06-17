<template>
  <section>
    <v-container>
      <v-stack>
        <app-section-descriptor
          title="Roadmap"
          heading="Neatio 2023 Roadmap"
          description="At Neatio, our relentless pursuit is to establish the forefront of payment systems. Discover our remarkable achievements and ongoing endeavors below. Inspired? Join us in shaping the future! Together, we can make Neatio the epitome of advancement in the realm of payments."
          style="max-width: 58rem"
        />
      </v-stack>
    </v-container>
    <div class="roadmap-container">
      <v-image
        path="images/roadmap-desktop.png"
        class="tablet-remove mobile-remove roadmap-desktop"
      />
      <div class="laptop-remove position-relative" style="text-align: center">
        <v-image path="images/roadmap-mobile-bg.png" class="roadmap-mobile" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Roadmap',
}
</script>

<style lang="css" scoped>
/* Imported this for getting helper classes laptop-remove and mobile-remove */
@import url('../lib/media-query-helper.css');

section {
  margin-top: 0 !important;
  padding: 6rem 0 0;
  background: radial-gradient(
    90.99% 90.99% at 4.06% 0%,
    rgba(150, 221, 226, 0.2) 0%,
    rgba(0, 0, 0, 0) 100%
  );

  @media (--viewport-small) {
    padding: 3rem 0 0;
  }
}

.roadmap-container {
  margin-top: 6rem;
  text-align: center;

  @media (--viewport-medium) {
    margin-top: 3rem;
  }
}

.roadmap-desktop {
  width: 100%;
  max-width: 1920px;
}

.roadmap-mobile {
  width: 100%;
  max-width: 375px;
}
</style>
