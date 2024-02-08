<template>
  <div class="done-card-container">
    <MoleculeDoneCard />
    <MoleculeDoneCard />
    <MoleculeDoneCard />
    <MoleculeDoneCard />
  </div>
</template>

<script>
import MoleculeDoneCard from "../molecules/cards/MoleculeDoneCard.vue";

export default {
  name: "OrganismDoneTasks",
  components: {
    MoleculeDoneCard,
  },
};
</script>

<style scoped>
.done-card-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>