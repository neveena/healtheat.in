<template>
  <div>
    <AppHeader />
    <nuxt />
    <AppFooter />
  </div>
</template>
<script>
import AppHeader from '@/components/AppHeader'
import AppFooter from '@/components/Footer'

export default {
  components: {
    AppHeader,
    AppFooter
  }
}
</script>
