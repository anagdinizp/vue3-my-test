<template>
  <div class="container">
    <MoleculeHeader />
    <MoleculeDoneCard />
  </div>
</template>

<script>
import MoleculeHeader from '../molecules/MoleculeHeader.vue';
import MoleculeDoneCard from '../molecules/MoleculeDoneCard.vue';

export default {
  name: "OrganismDoneTasks",
  components: {
    MoleculeHeader,
    MoleculeDoneCard
  },
};
</script>

<style>
.container {
  background: #000;
  color: #fff;
}
</style>