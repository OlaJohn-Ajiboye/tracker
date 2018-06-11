<template>
  <v-app id="inspire">
    <v-content>
      <v-container fluid fill-height>
        <v-layout align-center justify-center>
          <v-flex xs12 sm8 md4>
            <v-card class="elevation-12">
              <v-toolbar dark color="primary">
                <v-toolbar-title >Login Form</v-toolbar-title>
                <v-spacer></v-spacer>
                </v-toolbar>
                <v-card-text>
                <v-form>
                  <v-text-field prepend-icon="email" label="Email" type="mail" v-model='email'></v-text-field>
                  <v-text-field id="password" prepend-icon="lock" label="Password" type="password" v-model='password'></v-text-field>
                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn class='v-btn'  color="primary" @click = 'login'>Sign In</v-btn>
              </v-card-actions>
            </v-card>
            <br>
            <div class="danger-alert" v-html='error'/>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService'

export default {
  data () {
    return {
      email: '',
      password: '',
      error: null,
      success: null
    }
  },
  methods: {
  async login (){
   try {
      const response = await AuthenticationService.login ({
       email: this.email,
        password: this.password
          })
          } catch (error){
         this.error = error.response.data.error
    }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.danger-alert {
  color: red;
}
.success-alert {
  color: green;
}
.v-btn {
  border-radius: 5px;
}
</style>
