<template>
  <OrganismNewTasks />
</template>

<script>
import OrganismNewTasks from "./components/organisms/OrganismNewTasks.vue";

export default {
  name: "App",
  data() {
    return {
      inHome: {
        type: Boolean,
        default: true,
      },
    };
  },
  components: {
    OrganismNewTasks,
  },
  methods: {
    goToHomePage() {
      this.inHome == true;
      this.inDone == false;
      console.log("router to home page");
    },
    goToDonePage() {
      this.inHome == false;
      this.inDone == true;
      console.log("router to done page");
    },
  },
};
</script>

<style >
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
