<script>
import axsios from "axios";
import { store, api } from "./store";

export default {
  data() {
    return {
      title: "Front-End Boolfolio",
      projects: [],
      store,
    };
  },
  created() {
    axsios.get(api.baseUrl + "project").then((response) => {
      this.projects = response.data.data;
    });
  },
};
</script>

<template>
  <div class="container">
    <h1 class="mt-5">{{ title }}</h1>
    <h2>Projects:</h2>
    <div v-for="project in projects">
      <ul>
        <li><strong>Id: </strong> {{ project.id }}</li>
        <li><strong>Title: </strong> {{ project.title }}</li>
        <li><strong>Content: </strong> {{ project.content }}</li>
      </ul>
      <hr />
    </div>
  </div>
</template>

<style lang="scss">
@use "/src/scss/general.scss";
</style>
