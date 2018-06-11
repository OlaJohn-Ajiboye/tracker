<template>
  <v-toolbar fixed dark class='home' color="primary">
    <v-toolbar-title ><v-btn 
          flat 
          dark router 
          to='root' 
          >Tabtracker
          </v-btn>
          </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items>
          <v-btn 
          flat 
          dark
          router
          to="register"
          >Sign Up</v-btn>
          <!-- <v-btn flat>Link Two</v-btn>
      <v-btn flat>Link Three</v-btn> -->
      </v-toolbar-items>
      <v-toolbar-items>
          <v-btn 
          flat 
          dark
          router
          to="login"
          >Login</v-btn>
          <!-- <v-btn flat>Link Two</v-btn>
      <v-btn flat>Link Three</v-btn> -->
      </v-toolbar-items>
   </v-toolbar>
</template>

<script>
export default {
  data () {
    return {
     
    }
  },
  methods: {
   
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
