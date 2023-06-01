<script>
import AppFooter from './components/AppFooter.vue'
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter,
    AppMain,

  },
}
</script>

<template>
  <AppHeader />
  <AppMain />
  <div class="content">
    <h1>Content goes here</h1>
  </div>
  <AppFooter />
</template>

<style lang="scss">
@use './styles/partials/mixins.scss' as *;
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;

.content {
  height: 200px;
  @include center();
  background-color: #000;
  color: white;
}
</style>
