<script>
// import HeaderComponent from "./components/Header.vue";

export default {
  data() {
    return {
      title: "card",
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
    project: Object,
  },
};
</script>

<template>
  <div class="card">
    <div class="card-body">{{ project.name }}</div>
  </div>
</template>

<style lang="scss" scoped></style>
