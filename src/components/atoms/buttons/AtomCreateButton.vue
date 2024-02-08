<template>
  <button class="button" @click="createTask()">
    <AtomCreateIcon />
  </button>
</template>

<script>
import AtomCreateIcon from '../icons/AtomCreateIcon.vue';

export default {
  name: "AtomCreateButton",
  components: {
    AtomCreateIcon,
  },
  methods: {
    createTask() {
      this.$emit("createTask");
      console.log("create new task");
    },
  },
};
</script>

<style scoped>
.button {
  border: 0;
  background: none;
}
</style>