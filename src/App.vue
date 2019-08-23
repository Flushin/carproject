<template>
  <v-app id="sandbox">
    <v-navigation-drawer mini-variant app overflow v-model="toolbar"></v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon v-if="toolbar !== 'permanent'" @click.stop="toolbar = !toolbar">
      </v-app-bar-nav-icon>
      <v-toolbar-title>Car Project</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <HomeScreen/>
    </v-content>

    <v-footer :inset="footer.inset" app>
      <span class="px-4">&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>

  </v-app>
</template>

<script>
import HomeScreen from '@/components/HomeScreen.vue';

export default {
  name: 'App',
  components: {
    HomeScreen,
  },
  data: () => ({
    toolbar: false,
    footer: {
      inset: false,
    },
  }),
};
</script>
