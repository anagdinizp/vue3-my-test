<template>
  <div class="date-container">
    <h1 class="day">5</h1>
    <div class="day-month-year-container">
      <h3 class="month-year">2024-2</h3>
      <h3 class="day-name">Mon</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "AtomDate",
  data() {
    return {
      milisecDate: {
        type: Number,
        default: Date.now()
      },
    }
  }
};
</script>

<style scoped>
.date-container {
  display: flex;
  flex-direction: row;
  gap: 10px;
  align-items: center;
}
.day {
  font-weight: 700;
  color: #1b1c1f;
  font-size: 44px;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
.day-month-year-container {
  display: flex;
  flex-direction: column;
  font-family: Arial, Helvetica, sans-serif;
  text-align: left;
  justify-content: space-around;
}
.month-year {
  font-size: 13px;
  font-weight: 100;
  margin: 0px
}
.day-name {
  font-size: 13px;
  font-weight: 100;
  margin: 0px
}
</style>