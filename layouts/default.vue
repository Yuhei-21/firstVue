<template>
  <v-app dark>
    <v-toolbar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-toolbar-side-icon @click="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <nuxt-link :to="page.to" class="ml-3" v-for="page in pages" :key="page.title">{{page.title}}</nuxt-link>
    </v-toolbar>
    <v-content>
      <nuxt />
      
    </v-content>
    <v-footer
      :fixed="fixed"
      app
    >
      <span>&copy; 2019</span>
      
    </v-footer>
  </v-app>
</template>



<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      pages:[
        {
          title: '完成までの流れ',
          to: '/'
        },
        {
          title: '施工事例',
          to: '/'
        },
        {
          title: '会社概要',
          to: '/'
        },
        {
          title: 'お問い合わせ',
          to: '/'
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: '株式会社服部エクステリア'
    }
  }
}
</script>