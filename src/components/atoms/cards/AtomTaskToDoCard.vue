<template>
  <div class="container">
    <div class="task-card" v-for="task in tasksToDoList" :key="task">
      <input
        v-model="doneTasks"
        type="checkbox"
        :value="task"
        class="checkbox"
      />
      <p class="task-content">{{ task }}</p>
    </div>
    {{ doneTasks }}
  </div>
</template>

<script>
export default {
  name: "AtomTaskToDoCard",
  data() {
    return {
      doneTasks: [],
      tasksToDoList: ["take a nap", "eat a pizza", "take a shower"],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-inline: 10px;
}
.task-card {
  background-color: #ffffff;
  justify-content: space-between;
  color: black;
  font-size: larger;
  width: 327px;
  max-width: 327px;
  height: 59px;
  display: flex;
  justify-content: start;
  align-items: center;
  box-shadow: 0px 4px 40px 0px #0f163a14;
  margin-bottom: 10px;
  padding-left: 15px;
}
.task-content {
  color: #333333;
  font-size: 16px;
  padding-left: 8px;
}
.checkbox {
  appearance: none;
  padding: 0.5rem;
  border: 0.1rem solid #979797;
  border-radius: 100%;
  cursor: pointer;
}
.checkbox:checked::before {
  border: 0.5rem solid #24a19c;
  clip-path: circle(50% at 50% 50%);
}
.checkbox::before {
  border: 0.5rem solid #24a19c;
}
</style>