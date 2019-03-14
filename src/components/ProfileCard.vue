<template>
  <v-container>
    <v-layout align-center column wrap>
      <v-flex>
        <img :src="user.photoURL">
      </v-flex>
      <v-flex>
        <div>{{ user.name }}</div>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'ProfileCard',
  props: {
    user: Object
  }
}
</script>
