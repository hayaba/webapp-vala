<template>
  <div id="app">
    <v-container fluid>
      <myheader />
      <!-- <myModal /> -->
      <router-view></router-view>
      <myfooter />
    </v-container>
  </div>
</template>

<script>
import header from "./components/header";
import footer from "./components/footer";
// import modal from "./components/modal";

export default {
  components: {
    myheader: header,
    myfooter: footer
    // myModal: modal,
  },
  data() {
    return {
      isModalVisible: false
    };
  },
  methods: {
    close() {
      this.$emit("close");
    },
    showModal() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    }
  }
};
</script>

<style >
html,
body,
#app {
  font-family: "Roboto", sans-serif;
  background-color: #f5f5f5;
}

.container {
  padding: 0;
}
</style>