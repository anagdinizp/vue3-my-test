<template>
  <MoleculeHomeTitle />
  <AtomTaskToDoCard />
</template>

<script>
import AtomTaskToDoCard from "../atoms/cards/AtomTaskToDoCard.vue";
import MoleculeHomeTitle from "../molecules/MoleculeHomeTitle.vue";

export default {
  name: "OrganismHome",
  components: {
    MoleculeHomeTitle,
    AtomTaskToDoCard,
  }
};
</script>

<style scoped>
</style>