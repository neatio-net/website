<template>
  <div>
    <v-text font="sans" size="1rem">
      <a href="/terms/"
              >
    <v-text size="1rem">Terms</v-text></a
            >
      © {{ currentYear }} Neatio.
    </v-text>
  </div>
</template>

<script>
export default {
  name: 'AppCopyright',
  computed: {
    currentYear() {
      return new Date().getFullYear()
    },
  },
}
</script>

<style lang="css" scoped>
div {
  padding-bottom: 2.5rem;
  text-align: center;
}
</style>
