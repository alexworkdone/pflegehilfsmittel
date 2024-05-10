<template>
  <header class="wrapper">
    <div class="header">
      <button
        v-if="!isDesktop"
        class="menu-burger"
        :class="{ active: isShowMenu }"
        @click.stop="isShowMenu = !isShowMenu"
      >
        <div class="menu-burger-in">
          <div class="menu-burger_1"></div>
          <div class="menu-burger_2"></div>
          <div class="menu-burger_3"></div>
        </div>
      </button>

      <img class="logo" :src="require(`@images/logo.png`)" alt="logo" />

      <ul
        class="menu-main"
        :class="{ 'menu-mobile': !isDesktop, active: isShowMenu }"
        @click.stop="isShowMenu = !isShowMenu"
      >
        <li><a href="#" class="menu-link">Die Software</a></li>
        <li><a href="#" class="menu-link">Preise</a></li>
        <li><a href="#" class="menu-link">Blog</a></li>
        <li><a href="#" class="menu-link">Boxenkonfigurator</a></li>
      </ul>

      <button class="btn btn-medium btn-primary" @click="goToAccount">
        <template v-if="!isDesktop">
          <icon-user />
        </template>
        <template v-else>Mein Account</template>
      </button>
    </div>
  </header>
</template>

<script>
import IconUser from '@images/components/icon-user.vue'

export default {
  name: 'GHeader',

  components: {
    IconUser,
  },

  data: () => ({
    widthWindow: 0,

    isShowMenu: false,
    isToggleMenuLang: false,
  }),

  computed: {
    isDesktop() {
      return this.widthWindow >= 900
    },

    isMobile() {
      return this.widthWindow <= 768
    },
  },

  mounted() {
    window.addEventListener('resize', this.resizeWidth)
    this.resizeWidth()
  },

  beforeUnmount() {
    window.removeEventListener('resize', this.resizeWidth)
  },

  methods: {
    goToAccount() {
      console.log('goToAccount')
    },

    resizeWidth() {
      this.widthWindow = document.body.clientWidth
    },
  },
}
</script>
