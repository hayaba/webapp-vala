<template>
  <div class="modal-backdrop">
    <div class="modal">
      <header>
        <v-layout row wrap>
          Login Form
          <v-spacer></v-spacer>
          <button type="button" class="btn-close" @click="closemodal">x</button>
        </v-layout>
      </header>
      <v-flex>
        <v-text-field type="email" label="E-mail"></v-text-field>
        <v-text-field type="password" label="Password"></v-text-field>
      </v-flex>
      <v-btn class="btn-login">Login</v-btn>
    </div>
  </div>
</template>

<script>
export default {
  name: "Login",

  methods: {
    close() {
      this.$emit("close");
    }
  }
};
</script>

<style scoped>
.modal-backdrop {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 999;
}

.modal {
  width: 400px;
  height: 300px;
  padding: 5px 30px 30px 30px;
  background: #ffffff;
  box-shadow: 2px 2px 10px 1px;
  overflow-x: auto;
  display: flex;
  flex-direction: column;
}
.btn-close {
  border: none;
  font-size: 20px;
  cursor: pointer;
  background: transparent;
}

.btn-login {
  color: #000000;
  background-color: #e6d698;
  border: 4px solid #e6d698;
}
</style>