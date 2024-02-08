<template>
  <div class="container">
    <AtomPreviousButton @previous="previous()" />
    <h2 class="create-task-title">Create task</h2>
  </div>
</template>

<script>
import AtomPreviousButton from "../atoms/AtomPreviousButton.vue";

export default {
  name: "MoleculeNewTitle",
  components: {
    AtomPreviousButton,
  },
  methods: {
    previous() {
      console.log("router to home - previous");
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: start;
}
.create-task-title {
  font-size: 18px;
  font-weight: 500;
  line-height: 22px;
  letter-spacing: 0px;
  text-align: center;
  color: #1b1c1f;
  justify-self: center;
  justify-content: center;
  align-self: center;
}
</style>