<template>
  <v-layout justify-center align-center column class="pa-5">
    <div>このサービスは開発中です...!</div>
    <div>This service is under development...!</div>
    <v-flex>
      <img style="width: 120px; height: auto;" alt="logo" src="../assets/space_rocket.png">
    </v-flex>
    <v-flex>
      <profile-card :user="user"></profile-card>
    </v-flex>
    <v-flex>
      <v-btn @click="loginWithTwitter" color="light-blue white--text">Twitter Login</v-btn>
    </v-flex>
  </v-layout>
</template>

<script>

import firebase from 'firebase'

// @ is an alias to /src
import ProfileCard from '@/components/ProfileCard.vue'

export default {
  name: 'home',
  data () {
    return {
      user: {
        name: "",
        photoURL: ""
      }
    }
  },
  methods: {
    loginWithTwitter() {
      const provider = new firebase.auth.TwitterAuthProvider()
      firebase.auth().signInWithPopup(provider).then(result => {
        if (result.user) {
          console.log("assingning user...")
          this.user.name = result.user.displayName
          this.user.photoURL = result.user.photoURL
        }
      })
    }
  },
  components: {
    ProfileCard
  }
}
</script>
