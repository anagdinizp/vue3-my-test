<template>
  <MoleculeHeader :homePage="inHome" @home="goToHomePage()" @done="goToDonePage()" />
  <MoleculeNewTitle />
  <AtomCreateTaskInput />
  <AtomCreateButton />
</template>

<script>
import MoleculeHeader from './components/molecules/MoleculeHeader.vue'
import MoleculeNewTitle from './components/molecules/MoleculeNewTitle.vue';
import AtomCreateTaskInput from './components/atoms/AtomCreateTaskInput.vue'
import AtomCreateButton from './components/atoms/AtomCreateButton.vue';

export default {
  name: "OrganismNewTasks",
  components: {
    MoleculeHeader,
    MoleculeNewTitle,
    AtomCreateTaskInput,
    AtomCreateButton
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

<style scoped>

</style>