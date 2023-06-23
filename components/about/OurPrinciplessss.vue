<template>
  <section>
    <v-container>
      <v-stack justify="space-between" md-direction="column">
        <v-stack direction="column" style="max-width: 38rem">
          <v-heading :level="1">
            What Neatio Solves and Provides
          </v-heading>
          <app-section-descriptor
            description="Making use of machine learning and blockchain technologies, Neatio helps your business to enhance cybersecurity, automate tasks, optimize supply chain management, improve customer service, augment your marketing strategies and improve HR and talent management."
          />
        </v-stack>
        <div class="illustration-container">
          <v-image
            class="principles-illustration"
            path="images/neatio-services.png"
          />
        </div>
      </v-stack>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'OurPrinciples',
}
</script>

<style lang="css" scoped>
@import url('../lib/media-query-helper.css');

section {
  @media (--viewport-small) {
    margin-top: 0 !important;
  }
}

.illustration-container {
  position: relative;
}

.illustration-container::before {
  content: '';
  position: absolute;
  inset: -20%;
  z-index: -1;
  background: radial-gradient(
    50% 40% at 50% 40%,
    rgba(248, 81, 142, 0.2) 0%,
    rgba(0, 0, 0, 0) 100%
  );
}

.principles-illustration {
  width: 100%;
  max-width: 28rem;
  align-self: center;

  @media (--viewport-medium) {
    max-width: 20rem;
    margin: 2rem auto;
  }
}
</style>
