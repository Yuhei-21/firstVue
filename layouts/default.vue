<template>
  <v-app dark>
    <v-app-bar :clipped-left="clipped" fixed app color="#ffffff">
      <img src="hattorilogo.jpg" class="mr-1" >
      <v-toolbar-title @click="$router.push('/')"> {{title}} </v-toolbar-title>
      <v-spacer />
      <nuxt-link :to="page.to" class="ml-3" v-for="page in pages" :key="page.title">{{page.title}}</nuxt-link>
    </v-app-bar>
    <v-content>
      <nuxt />
      
    </v-content>
    <v-footer :fixed="fixed" app color="#ffffff" class="d-flex justify-end">
      <span class="d-flex justify-center">お問い合わせ</span>
      <v-icon class="icon">mdi-cellphone</v-icon>080-1508-3239
      <v-icon class="icon">mdi-deskphone</v-icon>072-477-4449
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