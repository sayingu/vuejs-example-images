<template>
  <div>
    <Header />
    <div class="ui container">
      <router-view />
    </div>
  </div>
</template>

<script>
import Header from "./components/AppHeader";

export default {
  name: "app",
  components: {
    Header
  }
};
</script>

<style>
</style>
