<template>
  <section>
    <v-container>
      <v-carousel ref="carousel" class="carousel-container">
        <template #slides>
          <div
            v-for="(slide, index) in slides"
            :key="'testimonial-carousel-' + index"
          >
            <v-stack md-direction="column" align="center" md-align="start">
              <v-image
                :path="slide.companyLogo"
                class="testimonial-illustration"
              />
              <v-stack direction="column">
                <v-heading :level="4" :weight="600" class="testimonial-quote">
                  “{{ slide.quote }}”
                </v-heading>
                <v-stack md-direction="column" align="baseline">
                  <v-text :weight="600" class="testimonial-quoted-by">
                    {{ slide.quotedBy }},&nbsp;
                  </v-text>
                  <v-text color="secondary" :weight="300" class="designation">
                    {{ slide.designation }}
                  </v-text>
                </v-stack>
              </v-stack>
            </v-stack>
          </div>
        </template>
        <v-stack md-direction="column" align="center" md-align="start">
          <v-image
            :path="slides[0].companyLogo"
            class="testimonial-illustration transparent"
          />
          <v-stack class="icons" md-justify="center">
            <v-image
              path="icons/arrow-left.svg"
              @click.stop="$refs.carousel.changeSlide(-1)"
            />
            <v-image
              path="icons/arrow-right.svg"
              @click.stop="$refs.carousel.changeSlide(1)"
            />
          </v-stack>
        </v-stack>
      </v-carousel>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'Testimonials',
  data() {
    return {
      slides: [
        {
          quote:
            'Nice words',
          quotedBy: 'Name',
          designation: 'CEO of Company',
          companyLogo: 'images/testimonials/unmarshal.png',
        },

      ],
    }
  },
}
</script>

<style lang="postcss" scoped>
@import url('../lib/media-query-helper.css');

section {
  background: #000 no-repeat;
  background-size: cover;
  box-shadow: 0 1rem 2rem 0.5rem black, 0 -1rem 2rem 0.5rem black;
  padding: 6rem 0;

  @media (--viewport-medium) {
    background: #000 no-repeat;
    background-size: cover;
    padding: 2rem 0;
  }
}

/* Need to add height because Carousel component has relative position */
.carousel-container {
  width: 100%;
  height: 100vh;
  max-height: 20rem;

  @media (--viewport-large) {
    max-height: 30rem;
  }

  @media (--viewport-medium) {
    max-height: 32rem;
  }
}

.testimonial-quote {
  font-size: 1.5rem;
  line-height: 2rem;
  margin-top: 0;

  @media (--viewport-medium) {
    font-size: 1.25rem;
    line-height: 1.5rem;
  }

  @media (--viewport-small) {
    font-size: 1rem;
    line-height: 1.2rem;
  }
}

.testimonial-quoted-by {
  font-size: 1.375rem;
  line-height: 2rem;

  @media (--viewport-medium) {
    font-size: 0.875rem;
    line-height: 1.375rem;
  }
}

.designation {
  font-size: 1rem;
  line-height: 1.5rem;

  @media (--viewport-medium) {
    font-size: 0.75rem;
    line-height: 1.125rem;
    margin-left: 0;
  }
}

.testimonial-illustration {
  margin-right: 10vw;
  max-width: 16rem;

  @media (--viewport-medium) {
    margin: 1rem auto;
  }

  @media (--viewport-small) {
    margin: 1rem auto;
    max-width: 12rem;
  }
}

.transparent {
  opacity: 0;
}

.icons {
  position: relative;
  margin-top: 18rem;
  width: 100%;

  @media (--viewport-large) {
    position: relative;
    margin-top: 26rem;
  }

  @media (--viewport-medium) {
    position: absolute;
    bottom: 0;
  }
}

.icons > * {
  object-fit: cover;
  cursor: pointer;
}

.icons > * + * {
  margin-left: 1rem;
}
</style>
