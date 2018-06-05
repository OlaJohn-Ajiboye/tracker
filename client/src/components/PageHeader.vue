<template>
  <v-toolbar fixed dark color="primary">
    <v-toolbar-title >Tabtracker</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items class="hidden-sm-and-down">
      <router-link to="home">
        <v-btn>
          SIGNUP
        </v-btn>
      </router-link>

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
