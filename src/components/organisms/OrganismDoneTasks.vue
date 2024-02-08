<template>
  <MoleculeHeader
    :homePage="inHome"
    @home="goToHomePage()"
    @done="goToDonePage()"
  />
  <div class="done-card-container">
    <MoleculeDoneCard />
    <MoleculeDoneCard />
    <MoleculeDoneCard />
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
.done-card-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>