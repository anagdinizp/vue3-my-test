<template>
  <div class="container">
    <AtomTaskDoneCardHeader />
    <div>done tasks</div>
  </div>
</template>

<script>
import AtomTaskDoneCardHeader from '../atoms/AtomTaskDoneCardHeader.vue';

export default {
  name: "MoleculeDoneCard",
  components: {
    AtomTaskDoneCardHeader
  }
};
</script>

<style>
.container {
  background: #000;
  color: #fff;
}
</style>