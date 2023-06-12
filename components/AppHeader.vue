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
      // headerCta: {
      //   label: 'Start Building',
      //   link: process.env.NEATIO_DASHBOARD_URL,
      // },
      menuItems: [
      {
          name: 'Team',
          link: '/about/',
        },
        {
          name: 'Whitepaper',
          link: '/whitepaper/',
          // external: true,
        },
        {
          name: 'Roadmap',
          link: '/tech/',
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
  background-color: #0f0f0f;
}
</style>
