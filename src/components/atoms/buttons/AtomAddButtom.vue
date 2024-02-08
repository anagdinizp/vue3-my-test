<template>
  <button class="add-button" @click="goToCreateTaskPage()">
    <span class="add">+</span>
  </button>
</template>

<script>
export default {
  name: "AtomAddButton",
  methods: {
    goToCreateTaskPage() {
      this.$emit("createTask");
      console.log("button to create task page");
    }
  }
};
</script>

<style scoped>
.add-button {
  background: #24a19c;
  width: 48px;
  height: 48px;
  border: #24a19c;
  border-radius: 100%;
}
.add {
  font-size: 36px;
  color: white;
  font-weight: 200;
  font-family: 'Courier New', Courier, monospace;
}
</style>