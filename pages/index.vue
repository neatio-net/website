<template>
  <main>
    <HomeHeroSection />
    <HomeOurServices />
    <HomeOurMission />
    <HomeRoadmap />
  </main>
</template>

<script>

export default {
  layout: 'page',
}
</script>

<style lang="css" scoped>
@import url('../components/lib/media-query-helper.css');

main {
  overflow-x: hidden;
}

main > * {
  margin-top: 6rem;
}
</style>
