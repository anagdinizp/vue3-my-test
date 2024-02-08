<template>
  <div>
    <MoleculeHeader
      :homePage="inHome"
      @home="goToHomePage()"
      @done="goToDonePage()"
    />
    <MoleculeDoneCard />
  </div>
</template>

<script>
import MoleculeHeader from "../molecules/MoleculeHeader.vue";
import MoleculeDoneCard from "../molecules/cards/MoleculeDoneCard.vue";

export default {
  name: "OrganismDoneTasks",
  components: {
    MoleculeHeader,
    MoleculeDoneCard,
  },
  data() {
    return {
      inHome: {
        type: Boolean,
        default: false,
      },
    };
  },
};
</script>

<style scoped>
</style>