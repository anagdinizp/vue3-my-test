<template>
  <div class="container">
    <AtomDate />
    <AtomAddButton @createTask="goToCreateTaskPage()" />
  </div>
</template>

<script>
import AtomDate from '../atoms/AtomDate.vue';
import AtomAddButton from '../atoms/buttons/AtomAddButtom.vue';

export default {
  name: "MoleculeHomeTitle",
  components: {
    AtomDate,
    AtomAddButton
  },
  methods: {
    goToCreateTaskPage() {
      this.$router.push('/new')
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