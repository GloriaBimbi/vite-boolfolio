<script>
import { api } from "../store";
import ProjectCard from "../components/ProjectCard.vue";

export default {
  data() {
    return {
      project: null,
    };
  },

  creted() {
    const projectId = this.$route.params.id;
    axios.get(api.baseUrl + "projects/${projectId}").then((response) => {
      this.porject = response.data;
    });
  },

  props: { isDetail: Boolean },
  components: { ProjectCard },
};
</script>

<template>
  <h1 class="my-5">Project {{ $route.params.id }}</h1>
  <project-card :project="project" :isDetail="true" />
</template>

<style lang="scss" scoped>
@use "/src/scss/general.scss";
</style>
