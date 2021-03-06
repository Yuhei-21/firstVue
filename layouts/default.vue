<template>
  <v-app dark>
    <v-app-bar :clipped-left="clipped" fixed app >
      <img src="hattorilogo.jpg" class="mr-1" >
      <v-toolbar-title>{{title}}</v-toolbar-title>
      <v-spacer />
      <nuxt-link :to="page.to" class="ml-3" v-for="page in pages" :key="page.title">{{page.title}}</nuxt-link>
    </v-app-bar>
    <v-content>
      <nuxt />
      
    </v-content>
    <v-footer :fixed="fixed" app >
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
          to: '/completionflow'
        },
        {
          title: '施工事例',
          to: '/example'
        },
        {
          title: '会社概要',
          to: '/description'
        },
        {
          title: 'お問い合わせ',
          to: '/contact'
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: '株式会社服部エクステリア',
    }
  }
}
</script>