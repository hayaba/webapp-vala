<template>
  <div id="login-form">
    <v-row>
      <v-col class="form" md="6">
        <header>
          <h3>Login Form</h3>
        </header>
        <v-flex>
          <v-text-field type="email" label="E-mail"></v-text-field>
          <v-text-field type="password" label="Password"></v-text-field>
          <a href>Forgot your passward</a>

          <v-btn @click.prevent="signIn()">login</v-btn>
          <v-btn @click.prevent="signOut()">log out</v-btn>
        </v-flex>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import firebase from 'firebase/app'
 import 'firebase/firestore'

export default {
  data() {
    return {
      email: "",
      passward: ""
    };
  },
  methods: {
    signIn() {
      firebase.auth().signInwithEmailAndPassword(this.email, this.passward).then(() => {
          this.$router.replace('/')
      })
      .catch(function(error) {
          var errorCode = error.code;
          var errorMessage = error.message;
          if (errorCode === 'auth/wrong-password') {
              alert ("wrong password")
          } else {
              alert (errorMessage)
          }
          console.log(error)
      })
    },
    signOut() {}
  }
};
</script>

<style lang="scss" scoped>
#login-form {
  height: 400px;
  background-image: linear-gradient(#b3c6cc, #e9e9e9, #e9e9e9);
  display: flex;
  align-items: center;
}

.form {
  margin: 20px;
}

h3 {
  padding: 10px 0;
}

a {
  color: darkblue;
  padding: 10px 0 20px 0;
  text-decoration: underline;
  font-size: small;
}
</style>