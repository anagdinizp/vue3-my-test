<template>
  <button class="button" @click="createTask()">Create</button>
</template>

<script>
export default {
  name: "AtomCreateButton",
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
  background: #24a19c;
  color: #ffffff;
  width: 327px;
  height: 56px;
  padding: 20px;
  border-color: #24a19c;
  border-radius: 16px;
  font-size: 18px;
  font-weight: 400;
  line-height: 22px;
  letter-spacing: 0px;
  text-align: center;
}
</style>