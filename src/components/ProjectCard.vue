<script>
export default {
  props: { project: Object },
};
</script>

<template>
  <div class="card" style="width: 18rem">
    <img
      v-if="project.image != null"
      :src="project.image"
      class="card-img-top"
      alt="project image"
    />
    <div class="card-body">
      <h5 class="card-title">{{ project.title }}</h5>
      <p class="card-text">{{ project.content }}</p>
      <hr />
      <div class="type">Type: {{ project.type.label }}</div>
      <router-link
        class="btn btn-primary mt-4"
        :to="{ name: 'projects.show', params: { id: project.id } }"
      >
        Show More
      </router-link>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "/src/scss/general.scss";
</style>
