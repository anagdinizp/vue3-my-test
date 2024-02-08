<template>
  <div class="container">
    <div class="label-container">
      <label class="create-task-label">task</label>
    </div>

    <input v-model="task" type="text" class="create-task-input" />
  </div>
</template>

<script>
export default {
  name: "AtomCreateTaskInput",
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.create-task-input {
  width: 327px;
  height: 56px;
  margin-inline: 10px;
  border-radius: 6px;
  border: 1px solid #e0e5ed;
  margin-bottom: 40px;
  padding-inline: 10px;
}
.label-container{
  display: flex;
  justify-items: flex-start;
  padding-left: 10px;
}
.create-task-label {
  font-size: 16px;
  font-weight: 400;
  line-height: 20px;
  letter-spacing: 0em;
  text-align: start;
  color: #1b1c1f;
  margin-bottom: 10px;
}
</style>