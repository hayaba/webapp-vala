<template>
  <div class="overflow-hidden">
    <v-toolbar>
      <v-toolbar-side-icon>
        <router-link to="/">
          <v-img src="@/assets/logo.png" width="46px"></v-img>
        </router-link>
      </v-toolbar-side-icon>
      <v-spacer></v-spacer>

      <v-toolbar-items class="buttons">
      
        <router-link tag="li" active-class="active" to="/" exact>
          <a>Home</a>
        </router-link>

        <router-link tag="li" active-class="active" to="/About">
          <a>About</a>
        </router-link>

        <router-link tag="li" active-class="active" to="/Booking">
          <a>Booking</a>
        </router-link>

        <router-link tag="li" active-class="active" to="/Login">
          <a>Login</a>
        </router-link>

        <!-- <button type="button" class="btn" @click="showModal">Login</button>
        <modal v-show="isModalVisible" @close="closeModal" />-->
      </v-toolbar-items>

      <v-app-bar-nav-icon
        id="menu-nav-btn"
        @click.stop="sideNav = !sideNav"
        class="d-flex d-sm-none !important"
      ></v-app-bar-nav-icon>
    </v-toolbar>

    <v-navigation-drawer v-model="sideNav" absolute temporary right>
      <v-list-item-group>
        <router-link to="/">
          <v-list-item>Home</v-list-item>
        </router-link>

        <router-link to="/About">
          <v-list-item>About</v-list-item>
        </router-link>

        <router-link to="/Booking">
          <v-list-item>Booking</v-list-item>
        </router-link>

        <router-link to="/Login">
          <v-list-item>Login</v-list-item>
        </router-link>

        <!-- <v-list-item>
          <button id="show-modal" @click="showModal = true">Login</button>
          <modal v-show="isModalVisible" @close="closeModal" />
        </v-list-item>-->
      </v-list-item-group>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: "Login",

  data() {
    return {
      sideNav: false
      //  isModalVisible: false
    };
  }
};
</script>

<style lang="scss">
// @import "./src/scss/variables.scss";

.v-application--wrap {
  flex: 1 1 auto;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  display: flex;
  flex-direction: column;
  max-width: 100%;
  position: relative;
}

.v-toolbar__content {
  background-color: #e6d698;
}

.v-toolbar__items {
  align-items: center;
}

.v-list-item {
  display: flex;
  justify-content: center;
}

@media only screen and (min-width: 600px) {
  #menu-nav-btn {
    display: none;
  }
  .v-toolbar__content,
  .v-toolbar__extension {
    padding: 4px 0px 4px 16px !important;
  }
}

@media only screen and (max-width: 600px) {
  .v-toolbar__items.buttons {
    display: none;
  }
  .buttons {
    visibility: hidden;
  }
}

ul {
  display: inline;
}

li {
 float: left;
  list-style-type: none;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  
}

a {
  display: block;
  text-decoration: none;
  color: #000000;
  padding: 22px;
}


li a:hover{
  background-color: #ccbe86;
  transition: ease-in 0.4s;
}

li.router-link-exact-active{
  background-color: #ccbe86;
}
</style>