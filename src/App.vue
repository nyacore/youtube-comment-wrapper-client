<template>
  <v-app>
    <v-app-bar color="deep-purple accent-4" app>
      <v-toolbar-title class="headline text-uppercase">
        <span>YOUTUBE</span>
        <span class="font-weight-light">COMMENTS WRAPPER</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  data: () => ({
    //
  }),
};
</script>
