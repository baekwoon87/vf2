<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-app-bar-nav-icon @click="drawer = !drawer" />
      <site-title :title="title"></site-title>
    </v-app-bar>
    <v-navigation-drawer app v-model="drawer">
    <site-menu></site-menu>
    </v-navigation-drawer>
    <v-content>
      <router-view/>
    </v-content>
    <site-footer :footer="footer"></site-footer>
  </v-app>
</template>

<script>
import SiteTitle from '@/components/site/title'
import SiteFooter from '@/components/site/footer'
import SiteMenu from '@/components/site/menu'
export default {
  components: {
    SiteTitle,
    SiteFooter,
    SiteMenu
  },
  name: 'App',
  data () {
    return {
      drawer: false,
      items: [],
      title: '나의 타이틀 입니다.',
      footer: '푸터입니다.'
    }
  }
}
</script>
