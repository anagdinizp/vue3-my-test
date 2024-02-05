<template>
  <div class="container">
    <MoleculeHeader />
    <MoleculeNewTitleVue />
    <AtomCreateTaskInputVue />
    <AtomCreateButtonVue />
  </div>
</template>

<script>
import AtomCreateButtonVue from '../atoms/AtomCreateButton.vue';
import AtomCreateTaskInputVue from '../atoms/AtomCreateTaskInput.vue';
import MoleculeNewTitleVue from '../molecules/MoleculeNewTitle.vue';
import MoleculeHeader from '../molecules/MoleculeHeader.vue';

export default {
  name: "OrganismNewTasks",
  components: {
    AtomCreateButtonVue,
    AtomCreateTaskInputVue,
    MoleculeNewTitleVue,
    MoleculeHeader
  },
};
</script>

<style>
.container {
  background: #000;
  color: #fff;
}
</style>