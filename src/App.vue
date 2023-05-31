<script>
import AppFooter from './components/AppFooter.vue'
import AppHeader from './components/AppHeader.vue'
export default {
  name: 'App',
  components: {
    AppFooter,
    AppHeader,
  }
}
</script>

<template>
  <AppHeader />
</template>

<style lang="scss">
@use './styles/partials/mixins.scss' as *;
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;
</style>
