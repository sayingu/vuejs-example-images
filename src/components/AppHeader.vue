<template>
  <div class="ui secondary pointing menu">
    <router-link to="/" class="active item">Image Storage</router-link>
    <div class="right menu">
      <template v-if="isLoggedIn">
        <router-link to="/" class="ui item">Galleries</router-link>
        <router-link to="upload" class="ui item">Upload</router-link>
        <a class="ui item" @click="logout">Logout</a>
      </template>
      <template v-else>
        <a class="ui item" @click="login">Login</a>
      </template>
    </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from "vuex";

export default {
  name: "AppHeader",
  computed: { ...mapGetters(["isLoggedIn"]) },
  methods: { ...mapActions(["login", "logout"]) }
};
</script>

<style scoped>
</style>
