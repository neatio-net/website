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
            <div>Payments Freedom Powered by Neatio.</div>            
          </v-heading>
          <v-stack direction="column">
            <app-section-descriptor
              description="Neatio will lead you into the new digital era. 
              Step forward with confidence as we revolutionize the way we transact, empowering individuals and businesses alike with the security and trust of the blockchain technology."
              class="hero-description"
            />
            <v-stack align="center" gap="1.5rem" sm-gap="1rem" wrap>
              <router-link to="/about/">
                <v-button label="DISCOVER" label-transform="uppercase" />
              </router-link>
              <router-link to="/careers/">
                <v-button
                  variant="outline"
                  label="JOIN US"
                  label-transform="uppercase"
                  class="secondary-button"
                />
              </router-link>
            </v-stack>
          </v-stack>
        </v-stack>
        <v-image
              class="hero-image"
              path="images/blockchain2.png"
            />     
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
    padding: 10px 0;
    margin-top: 0 !important;
  }
}

.hero-image {
  max-width: 36rem;
  width: 100%;



  @media (--viewport-medium) {
    margin-right: 0;
  }

  @media (--viewport-small) {
    margin-top: 2rem;
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
  max-width: 20ch;
}
</style>
