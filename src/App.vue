<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  data() {
    return {
      title: "Front-End Boolfolio",
    };
  },

  components: { AppHeader },
};
</script>

<template>
  <app-header />
  <div class="container">
    <router-view />
  </div>
</template>

<style lang="scss">
@use "/src/scss/general.scss";
</style>
