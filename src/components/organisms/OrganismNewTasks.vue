<template>
  <MoleculeHeader
    :homePage="inHome"
    @home="goToHomePage()"
    @done="goToDonePage()"
  />
  <MoleculeNewTitle />
  <div class="content-container">
    <div class="label-container">
      <label class="create-task-label">task</label>
    </div>

    <input v-model="task" type="text" class="create-task-input" />
    <AtomCreateButton />
  </div>
</template>

<script>
import MoleculeHeader from "../molecules/MoleculeHeader.vue";
import MoleculeNewTitle from "../molecules/MoleculeNewTitle.vue";
import AtomCreateButton from "../atoms/buttons/AtomCreateButton.vue";
import VueLocalStorage from "vue-local-storage";

export default {
  name: "OrganismNewTasks",
  components: {
    MoleculeHeader,
    MoleculeNewTitle,
    AtomCreateButton,
  },
  mixins: [VueLocalStorage.mixin],
  data() {
    return {
      task: [
        {
          id: {
            type: Number,
            default: Date.now(),
          },
          content: {
            type: String,
            default: "",
          },
          date: {
            type: String,
            default: Date.now(),
          },
        },
      ],
    };
  },
  mounted() {
    this.task = this.$localStorage.get("task") || [];
  },
  watch: {
    task(newValue) {
      this.$localStorage.set("task", newValue);
    },
  },
  methods: {
    goToHomePage() {
      this.inHome == true;
      console.log("router to home page");
    },
    goToDonePage() {
      this.inHome == false;
      console.log("router to done page");
    },
  },
};
</script>

<style scoped>
.content-container {
  display: flex;
  flex-direction: column;
  align-items: center;
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
.label-container {
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