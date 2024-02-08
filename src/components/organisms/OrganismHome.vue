<template>
  <MoleculeHeader :homePage="inHome" @home="goToHomePage()" @done="goToDonePage()" />
  <MoleculeHomeTitle />
  <AtomTaskToDoCard />
</template>

<script>
import MoleculeHeader from './components/molecules/MoleculeHeader.vue'
import AtomTaskToDoCard from './components/atoms/AtomTaskToDoCard.vue';
import MoleculeHomeTitle from './components/molecules/MoleculeHomeTitle.vue';

export default {
  name: "OrganismHome",
  data() {
    return {
      inHome: {
        type: Boolean,
        default: true,
      }
    };
  },
  components: {
    MoleculeHeader,
    MoleculeHomeTitle,
    AtomTaskToDoCard
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

<style scoped>


</style>