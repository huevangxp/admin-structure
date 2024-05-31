<template>
  <v-app style="background-color: #F0F5F9;" >
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      height="900"
      class="elevation-10 ml-6 mt-6 rounded-lg"
    >
      <v-card elevation="0" class="mx-auto">
        <v-card-title class="d-flex justify-center">
          <v-icon v-if="miniVariant == true" size="50px" color="teal">mdi-bitcoin</v-icon>
          <v-icon v-else size="100px" color="teal">mdi-bitcoin</v-icon>
        </v-card-title>
      </v-card>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      max-width="1200px"
      app
      :sticky="true"
      class="mt-6 mx-auto rounded-lg "
    >
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
        <v-icon large>mdi-{{ `${miniVariant ? 'sort-reverse-variant' : 'sort-variant'}` }}</v-icon>
      </v-btn>


      <v-toolbar-title style="font-weight: bold">{{ title }}</v-toolbar-title>
      <v-spacer />
      <v-btn
        icon
        color="red"
      >
        <v-icon>mdi-power</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-card elevation="0" max-width="1200" class="mx-auto pt-12" style="background-color: #F0F5F9;">
        <Nuxt />
      </v-card>
    </v-main>


  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Admin'
    }
  }
}
</script>

<style>
.scroll {
  position: sticky;
   top: -10px;
  top:20px;
  z-index: 1; /* Ensure it's above other elements */
}




</style>
