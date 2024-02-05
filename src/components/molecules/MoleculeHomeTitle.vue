<template>
  <div class="container">
    <AtomDate />
    <AtomAddButton />
  </div>
</template>

<script>
import AtomAddButton from '../atoms/AtomAddButtom.vue';
import AtomDate from '../atoms/AtomDate.vue';

export default {
  name: "MoleculeHomeTitle",
  components: {
    AtomDate,
    AtomAddButton
  }
};
</script>

<style>
.button {
  background: #000;
  color: #fff;
}
</style>