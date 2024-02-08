<template>
  <MoleculeHeader
    :homePage="inHome"
    @home="goToHomePage()"
    @done="goToDonePage()"
  />
  <MoleculeDoneCard />
  <MoleculeDoneCard />
  <MoleculeDoneCard />
  <MoleculeDoneCard />
</template>

<script>
import MoleculeHeader from "./components/molecules/MoleculeHeader.vue";
import MoleculeDoneCard from "./components/molecules/cards/MoleculeDoneCard.vue";

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
    MoleculeHeader,
    MoleculeDoneCard
  },
  methods: {
    goToHomePage() {
      this.inHome == true;
      console.log("router to home page");
    },
    goToDonePage() {
      this.inHome == false;
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
