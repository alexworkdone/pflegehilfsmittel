<template>
  <div class="error-page">
    <template v-if="error.statusCode === 404">
      <h2>Page not found</h2>

      <div class="error-page-404-wrap">
        <div class="flex error-page-404">
          <span class="text-primary-d">4</span>
          <span class="text-dark-c">0</span>
          <span class="text-primary-l">4</span>
        </div>
      </div>

      <a href="/" class="btn btn-big btn-primary m-t-16">Go home</a>
    </template>
    <h2 v-else>An error occurred</h2>
  </div>
</template>

<script>
export default {
  name: 'ErrorPage',

  components: {},

  layout: 'error',

  props: {
    error: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>

<style lang="scss">
.error-page {
  height: calc(
    100vh - var(--height-header) - calc(40px + var(--height-footer))
  );
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;

  h2 {
    font-size: 48px;
    font-weight: 700;
    line-height: 1;
  }

  &-404 {
    position: relative;
    z-index: 1;
    display: flex;
    height: 100%;
    justify-content: center;
    align-items: center;
    font-size: 230px;
    font-weight: 700;
    line-height: 1;

    &-wrap {
      position: relative;
      margin: 0 auto;
      width: 516px;
      flex: 1;
      max-height: 312px;
    }
  }
}

@media screen and (max-width: 768px) {
  .error-page-404 {
    font-size: 150px;

    &-wrap {
      width: 320px;
      max-height: 220px;
    }
  }
}
</style>
