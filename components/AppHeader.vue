<template>
  <header class="app-header">
    <v-header
      logo="images/nio3-logo.png"
   
      :menu-items="menuItems"
    />
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      headerCta: {
        label: 'Start Building',
        link: process.env.NEATIO_DASHBOARD_URL,
      },
      menuItems: [
        
      {
          name: 'About',
          link: '/about/',
        },
      // {
      //     name: 'Asknio',
      //     link: 'https://asknio.com',
      //     external: true,
      //   },
      {
          name: 'Blog',
          link: 'https://blog.neatio.net',
          external: true,
        },
        {
          name: 'Explorer',
          link: 'https://scan.neatio.net',
          external: true,
        },
        
        {
          name: 'Roadmap',
          link: '/tech/',
        },
        {
           name: 'Wallet',
           link: 'https://wallet.neatio.net',
           external: true,
         },
        
        {
          name: 'Whitepaper',
          link: 'https://neatio.net/whitepaper.pdf',
          external: true,
        },
      ],
    }
  },
}
</script>

<style scoped>
.app-header {
  position: sticky;
  top: 0;
  z-index: 100;
  background-color: #00000096;
}
</style>
