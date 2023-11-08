<script>
import ProjectListComponent from "./components/ProjectListComponent.vue";
import axios from "axios";

export default {
  data() {
    return {
      title: "APP",
      projects: [],
      api: {
        baseUrl: "http://127.0.0.1:8000/api/",
      },
    };
  },

  methods: {
    fetchProjects(uri = this.api.baseUrl + "project") {
      axios.get(uri).then((responce) => {
        this.projects = responce.data.data;
      });
    },
  },

  components: {
    ProjectListComponent,
  },

  // 	props:{
  // 		passaggioInfo: stringa,
  //  	 },

  created() {
    this.fetchProjects();
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
  <ProjectListComponent :projects="projects" />
</template>

<style lang="scss" scoped></style>
