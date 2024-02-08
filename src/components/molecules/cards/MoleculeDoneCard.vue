<template>
  <div class="container">
    <div class="container-card-header">
      <h3 class="card-header-title">2.5</h3>
      <h3 class="card-header-title">1 task</h3>
    </div>
    <div class="card-content">
      <AtomCheckedIcon />
      <p class="content">eat pizza with yago</p>
    </div>
  </div>
</template>

<script>
import AtomCheckedIcon from "../../atoms/icons/AtomCheckedIcon.vue";

export default {
  name: "MoleculeDoneCard",
  components: {
    AtomCheckedIcon,
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 280px;
  margin-bottom: 15px;
}
.container-card-header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  width: 280px;
  height: 36px;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
  background: #24a19c;
  padding-top: 2px;
  padding-bottom: 2px;
}
.card-header-title {
  font-size: 12px;
  font-weight: 400;
  line-height: 15px;
  letter-spacing: 0em;
  text-align: left;
  color: #ffffff;
  padding-inline: 15px;
}
.card-content {
  background: #ffffff;
  box-shadow: 0px 4px 40px 0px #0f163a14;
  height: fit-content;
  justify-content: flex-start;
  padding: 10px;
  display: flex;
  flex-direction: row;
  align-items: center;
}

.content {
  text-align: justify;
  margin-left: 15px;
}
</style>