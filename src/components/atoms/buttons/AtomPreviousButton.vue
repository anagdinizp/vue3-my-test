<template>
  <button class="button" @click="previous()">
    <AtomPreviousIcon />
  </button>
</template>

<script>
import AtomPreviousIcon from "../icons/AtomPreviousIcon.vue";

export default {
  name: "AtomPreviousButton",
  components: {
    AtomPreviousIcon,
  },
  methods: {
    previous() {
      this.$emit("previous");
      console.log("button back to home");
    },
  },
};
</script>

<style scoped>
.button {
  background-color: transparent;
  color: #1b1c1f;
  font-size: larger;
  border: 0;
  cursor: pointer;
}
</style>