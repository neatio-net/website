<template>
  <footer>
    <v-container>
      <v-stack
        align="center"
        justify="space-around"
        :grow="1"
        class="footer-logo-container"
      >
        <!-- <v-image class="serv-image" path="images/AI-bust.png" />
        <v-image path="images/footer-orbs.svg" class="position-absolute" /> -->
      </v-stack>
            <app-section-descriptor
        title="Contact"
        heading="GET IN TOUCH"
        description="Neatio team can be contacted either directly by email or alternatively through our social media channels.
        To get the fastest response we recommend to reach us on our Discord server where the developers, validators or our dedicated community members are always online."
        style="max-width: 64rem"
      />
      <v-stack
        justify="space-between"
        md-direction="column"
        md-align="center"
        class="footer-navigation-container"
      >

        <v-stack direction="column">
          <v-text font="sans" :weight="600" class="get-in-touch">
              Write to us
            </v-text>
          <a href="mailto:contact@neatio.net">
            <v-text font="sans" :weight="600" class="footer-mailing">
              contact@neatio.net
            </v-text>
          </a>
          <v-stack style="margin-top: 3rem" md-justify="space-evenly">
            <a href="https://twitter.com/neatio_net" target="_blank">
              <v-image
                path="images/social/twitter.png"
                class="footer-social-link"
                alt="Neatio Twitter"
              />
            </a>

            <a
              style="margin-left: 2rem"
              href="https://discord.neatio.net"
              target="_blank"
            >
              <v-image
                path="images/social/discord.png"
                class="footer-social-link"
                alt="Neatio Discord"
              />
            </a>
            <a
              style="margin-left: 2rem"
              href="https://t.me/neatio_net"
              target="_blank"
            >
              <v-image
                style="height: 44px; width: auto;"
                path="images/social/telegram.png"
                class="footer-social-link"
                alt="Neatio Telegram"
              />
            </a>
            <a
              style="margin-left: 2rem"
              href="https://github.com/neatio-net"
              target="_blank"
            >
              <v-image
                style="height: 44px; width: auto;"
                path="images/social/github.png"
                class="footer-social-link"
                alt="Neatio Github"
              />
            </a>

          </v-stack>

        </v-stack>

        <!-- Footer Links -->
        <!-- <v-stack
          class="footer-links-container"
          justify="space-between"
          :grow="1"
        >
          <v-stack direction="column" class="footer-links">
            <a href=""><v-text></v-text></a>
            <a href="/about/"><v-text>About</v-text></a>
            <a href="https://blog.neatio.net"><v-text>Blogger</v-text></a>
            <a href="/careers/"><v-text>Careers</v-text></a>

          </v-stack>
          <v-stack direction="column" class="footer-links">
            <a href=""><v-text></v-text></a>
            <a href="https://bitcointalk.org/index.php?topic=5377414"><v-text>Forum</v-text></a>
            <a href="https://www.reddit.com/r/neatio/"><v-text>Reddit</v-text></a>
            <a href="/terms/" target="_blank"><v-text>Terms</v-text></a
            >

          </v-stack>
        </v-stack> -->
      </v-stack>
    </v-container>
  </footer>
</template>

<script>
const NEATIO_DISCORD_URL = process.env.NEATIO_DISCORD_URL
const NEATIO_BOOK_DEMO_URL = process.env.NEATIO_BOOK_DEMO_URL

export default {
  name: 'AppFooter',
  data() {
    return {
      NEATIO_DISCORD_URL,
      NEATIO_BOOK_DEMO_URL,
    }
  },
}
</script>

<style lang="css" scoped>
@import url('./lib/media-query-helper.css');

footer {
  background-color: linear-gradient(to right,#212226, #243B55);
  background-size: cover;
  overflow-x: hidden;

  @media (--viewport-small) {
    background-color: #000;
    background-size: 100%;
  }
}

.footer-logo-container {
  padding: 0;
  position: relative;

  @media (--viewport-small) {
    padding: 0;
  }
}

.footer-logo {
  margin: 0 auto;
  width: 8rem;
  height: auto;

  @media (--viewport-medium) {
    width: 6rem;
  }
}

.footer-navigation-container {
  padding: 4rem 0;

  @media (--viewport-small) {
    padding: 2rem 0;
  }
}

.footer-links-container {
  max-width: 50%;

  @media (--viewport-medium) {
    width: 100%;
    margin-top: 2rem;
    max-width: unset;
  }
}

.footer-links > * + * {
  margin-top: 3rem;
}

.footer-social-link {
  width: 3rem;
}

a {
  text-decoration: none;
}

.footer-links a * {
  font-family: var(--font-sans);
  font-weight: 500;
  font-size: 1.25rem;
  line-height: 0.5rem;

  @media (--viewport-medium) {
    font-size: 1.125rem;
    line-height: 0.5rem;
  }
}

.footer-mailing {
  color: #fff;
  font-size: 1.5rem;
  line-height: 2.25rem;
}
.get-in-touch {
  font-size: 1.5rem;
  line-height: 2.25rem;
  color: #8D80FF;

  @media (--viewport-medium) {
    font-size: 1.125rem;
    line-height: 1.5rem;
  }
}

@media (--viewport-small) {
  .footer-logo-container > *:first-child {
    width: 40%;
  }

  .footer-logo-container > *:last-child {
    width: 150%;
  }
}

.book-demo-container {
  margin-top: 4rem;
}



.book-demo-description {
  max-width: 21rem;
  line-height: 1.5;
}

.book-demo-btn {
  width: 14rem;
  height: 3.25rem;
  margin-top: 2rem;
}
</style>
