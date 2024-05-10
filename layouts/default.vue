<template>
  <div>
    <g-header />

    <div class="main-section">
      <Nuxt />
    </div>

    <g-footer />
  </div>
</template>

<script>
import GHeader from '../components/GHeader.vue'
import GFooter from '../components/GFooter.vue'

export default {
  name: 'DefaultLayout',

  components: {
    GHeader,
    GFooter,
  },
}
</script>
