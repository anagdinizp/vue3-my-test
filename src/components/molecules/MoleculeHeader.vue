<template>
  <header class="header">
    <button
      :class="['button', { 'button-inPage': inHome }]"
      @click="goToHomePage()"
    >
      Today
    </button>
    <button
      :class="['button', { 'button-inPage': inDone }]"
      @click="goToDonePage()"
    >
      Done
    </button>
  </header>
</template>

<script>
export default {
  name: "MoleculeHeader",
  props: {
    homePage: {
      type: Boolean,
      default: true,
    }
  },
  data() {
    return {
      inHome: {
        type: Boolean,
        default: this.homePage,
      },
      inDone: {
        type: Boolean,
        default: !this.homePage,
      },
    };
  },
  methods: {
    goToHomePage() {
      this.$emit("home");
      this.inHome == true;
      this.inDone == false;
      console.log('botao na header, home', this.inHome);
      console.log(this.inDone);
    },
    goToDonePage() {
      this.$emit("done");
      this.inHome == false;
      this.inDone == true;
      console.log('botao na header, done',this.inHome);
      console.log(this.inDone);
    },
  },
};
</script>

<style scoped>
.header {
  background: #f6f7f9;
  color: #fff;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 42px;
  justify-content: flex-start;
  align-items: center;
  display: flex;
}
.button {
  background: transparent;
  color: #262626;
  font-size: 14px;
  height: 42px;
  border: 0;
  font-family: Arial, Helvetica, sans-serif;
  cursor: pointer;
  margin-left: 20px;

}
.button-inPage {
  color: #24a19c;
  border-bottom: 2px solid #24a19c;
}
.button::hover {
  content: "";
  color: #24a19c;
  border-bottom: 2px solid #24a19c;
}
</style>