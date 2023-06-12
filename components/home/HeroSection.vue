<template>
  <section class="hero-section">
    <v-container>
      <v-stack
        justify="space-between"
        md-direction="column-reverse"
        md-align="center"
        class="position-relative"
      >
        <v-stack direction="column" class="hero-content-container">
          <v-heading :level="1" class="hero-title">
            <div>Beyond Payments.</div>            
          </v-heading>
          <v-stack direction="column">
            <app-section-descriptor
              description="Unveiling the future of seemless payments. Neatio will lead you into the new digital era. 
              Step forward with confidence as we revolutionize the way we transact, empowering individuals and businesses alike with the security and trust of the blockchain tech."
              class="hero-description"
            />

            <v-stack align="center" gap="1.5rem" sm-gap="1rem" wrap>
              <a href="" target="_blank">
                <v-button label="Learn More" label-transform="uppercase" />
              </a>
              <a :href="NEATIO_URL" target="_blank">
                <v-button
                  variant="outline"
                  label="Get Involved"
                  label-transform="uppercase"
                  class="secondary-button"
                />
              </a>

            </v-stack>

          </v-stack>

        </v-stack>
        

     
      </v-stack>



    </v-container>

  </section>
</template>

<script>






const NEATIO_URL = process.env.NEATIO_BOOK_DEMO_URL
const NEATIO_DASHBOARD_URL = process.env.NEATIO_DASHBOARD_URL

export default {
  name: 'HeroSection',


  data() {
    return {
      isIntroPlaying: false,
      NEATIO_URL,
      NEATIO_DASHBOARD_URL,

     
    }
  },

}
</script>

<style lang="css" scoped>
@import url('../lib/media-query-helper.css');

.hero-section {
  padding: 0 0 6rem;


  @media (--viewport-small) {
    padding: 0;
    margin-top: 0 !important;
  }
}

.hero-description {
  margin-block: 2rem;
}

.hero-content-container {
  max-width: 38rem;
}

.hero-title {
  margin-block: 0;
  max-width: 12ch;
}
</style>
