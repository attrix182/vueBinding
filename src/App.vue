<template>
  <v-app>
    <v-app-bar
      app
      color="dark"
      dark
    >

<h2>Binding values</h2>
      <v-spacer></v-spacer>


    </v-app-bar>

    <v-main>
      <HelloWorld/>
    </v-main>
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
