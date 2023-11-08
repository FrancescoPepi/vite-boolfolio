<script>
import ProjectCardComponent from "./ProjectCardComponent.vue";

export default {
  data() {
    return {
      title: "Project List",
    };
  },

  // 	methods:{
  // 		myMethods(){
  // 			...
  // 		},
  // 	},

  components: {
    ProjectCardComponent,
  },

  props: {
    projects: Array,
  },
};
</script>

<template>
  <div class="container">
    <h2>{{ title }}</h2>
    <div class="row row-cols-3 g-4">
      <div class="col" v-for="project in projects">
        <ProjectCardComponent :project="project" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
