<template>
  <header class="header">
    <AtomHeaderButtons />
  </header>
</template>

<script>
import AtomHeaderButtons from '../atoms/AtomHeaderButtons.vue'

export default {
  name: 'MoleculeHeader',
  components: {
    AtomHeaderButtons
  }
};
</script>

<style>
  .header {
  background: #000;
  color: #fff;
  }
</style>