<script>
// import HeaderComponent from "./components/Header.vue";

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

  // components: {
  //	MyComponent,
  // },

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
        <div class="card">
          <div class="card-body">{{ project.name }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
