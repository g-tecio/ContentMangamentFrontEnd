<template>
  <v-app>
    <v-toolbar>
      <v-toolbar-title>
        <v-btn icon to="/"><v-icon> home </v-icon></v-btn>
        <!-- Estancias 2019 -->
        {{this.$store.state.title}}
      </v-toolbar-title>
      <v-spacer/>
      <v-toolbar-items>
        <!-- SOY UN COMENTARIO -->
        <v-icon>toc</v-icon>
      </v-toolbar-items>
    </v-toolbar>
      <v-container>
        <nuxt />
      </v-container>
   
  </v-app>
</template>

<script>
  export default {
    data() {
      return {
        clipped: false,
        drawer: true,
        fixed: false,
        items: [
          { icon: 'apps', title: 'Welcome', to: '/' },
          { icon: 'bubble_chart', title: 'Inspire', to: '/inspire' }
        ],
        miniVariant: false,
        right: true,
        rightDrawer: false,
        title: 'Vuetify.js'
      }
    }
  }
</script>
