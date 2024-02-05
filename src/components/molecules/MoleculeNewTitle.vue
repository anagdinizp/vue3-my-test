<template>
  <div class="container">
    <AtomPreviousButton />
    <h2>Create task</h2>
  </div>
</template>

<script>
import AtomPreviousButton from "../atoms/AtomPreviousButton.vue";

export default {
  name: "MoleculeNewTitle",
  components: {
    AtomPreviousButton,
  },
};
</script>

<style>
.container {
  background: #000;
  color: #fff;
}
</style>