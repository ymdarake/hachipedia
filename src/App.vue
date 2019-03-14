<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title>
        <span class="headline font-weight-bold">はちペディア</span>
        <span class="font-weight-light">β</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        flat
        href="http://www.hachimitsu-rocket.com"
        target="_blank"
      >
        <span class="mr-2">GO TO OFFICIAL SITE</span>
      </v-btn>
    </v-toolbar>

    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App'
}
</script>
