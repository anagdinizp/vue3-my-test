<template>
  <div class="container">
    <AtomDate />
    <AtomAddButton @createTask="goToCreateTaskPage()" />
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
  },
  methods: {
    goToCreateTaskPage() {
      console.log("router to create task page");
    }
  }
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding-inline: 10px;
  align-items: center;
}
</style>