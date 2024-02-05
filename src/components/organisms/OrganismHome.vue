<template>
  <div class="container">
    <MoleculeHeader />
    <MoleculeHomeTitle />
    <AtomTaskToDoCardVue />
  </div>
</template>

<script>
import AtomTaskToDoCardVue from '../atoms/AtomTaskToDoCard.vue';
import MoleculeHeader from '../molecules/MoleculeHeader.vue';
import MoleculeHomeTitle from '../molecules/MoleculeHomeTitle.vue';

export default {
  name: "OrganismHome",
  components: {
    MoleculeHeader,
    MoleculeHomeTitle,
    AtomTaskToDoCardVue
  },
};
</script>

<style>
.container {
  background: #000;
  color: #fff;
}
</style>