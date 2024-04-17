<script>
import axsios from "axios";
import { store, api } from "../store";
import ProjectCard from "./ProjectCard.vue";

export default {
  data() {
    return {
      store,
    };
  },
  created() {
    axsios.get(api.baseUrl + "project").then((response) => {
      store.projects = response.data.data;
    });
  },
  components: { ProjectCard },
};
</script>

<template>
  <h2 class="my-4">Projects:</h2>
  <div class="card-container d-flex flex-wrap gap-5">
    <project-card v-for="project in store.projects" :project="project" />
  </div>
</template>

<style lang="scss" scoped>
@use "/src/scss/general.scss";
</style>
