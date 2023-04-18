<template>
  <AppHeader />
  <AppFirstDisplay />
  <AppFooter/>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppFirstDisplay from './components/AppFirstDisplay.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  components: { AppHeader, AppFirstDisplay, AppFooter }
}
</script>

<style>
</style>
