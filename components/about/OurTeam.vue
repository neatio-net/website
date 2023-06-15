<template>
  <section style="margin-bottom: 10rem">
    <v-container>
      <v-stack justify="space-between">
        <app-section-descriptor
          title="Our team"
          heading="The Neatio Builders"
        />
      </v-stack>
      <v-stack
        justify="space-between"
        md-direction="column"
        class="member-container"
        wrap
      >
        <div
          v-for="member in executiveMembers"
          :key="member.name + member.designation"
        >
          <about-team-member :member="member" />
        </div>
      </v-stack>

    </v-container>
  </section>
</template>

<script>
export default {
  name: 'OurTeam',
  data() {
    return {
      executiveMembers: [
        {
          name: 'Silviu Georgescu',
          designation: 'Founder, Lead Developer',
          image: 'team',
          links: {
            linkedin: "https://www.linkedin.com/in/silviu-georgescu-3a679b201",
            github: "https://github.com/GSilviu",
            twitter: "https://twitter.com/silviugeo"
          },
        },
        {
          name: 'Angelo Gorreti',
          designation: 'Founder, Head Of Marketing',
          image: 'team',
          links: {
            twitter: "https://twitter.com/agoretti_"
          },
          },
        {
          name: 'Adrian Vasile',
          designation: 'Lead Frontend Developer',
          image: 'team',
          links: {
            github: "https://github.com/mrtizu",
            twitter: "https://twitter.com/mrtizu"
          },
          },
        {
          name: 'Luckas83',
          designation: 'Web3 Developer',
          image: 'team',
          links: {
            github: "https://github.com/Luckas83",
          },
        },

        {
          name: 'Emmanuel Akinroye',
          designation: 'Solidity Developer',
          image: 'team',
          links: {
            github: "https://github.com/Emma66886",
          },
        },

        {
          name: 'Gessius',
          designation: 'Graphic Designer',
          image: 'team',
          links: {
            github: "https://github.com/Gessius",
          },
        },
        {
          name: 'Adrian Munteanu',
          designation: 'Assistant Developer',
          image: 'team',
          links: {
            github: "https://github.com/adi-mun",
          },
        },
        {
          name: 'Daniel Munteanu',
          designation: 'Advisor',
          image: 'team',
          links: {
           
          },
        },

      ],
    }
  },
}
</script>

<style lang="css" scoped>
@import url('../lib/media-query-helper.css');
.member-container {
  margin: 1rem 0;
  text-align: center;
  @media (--viewport-medium) {
    text-align: start;
  }
}
.member-container > * {
  margin: 1rem 0;
  flex: 1 0 33%;
}
.other-members {
  max-height: 0;
  opacity: 0;
  overflow: hidden;
  transition: max-height 0.4s, opacity 0.8s;
}
.expanded {
  opacity: 1;
  max-height: 100%;
}
@media (--viewport-medium) {
  .member-container > * + * {
    margin-top: 1rem;
  }
}
</style>