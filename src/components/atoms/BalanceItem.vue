<template>
  <div class="balance-item">
    <div class="text-container">
      <div class="title-container">
        <img :src="icon" :alt="title" style="color: black; margin-bottom: 10px" />
        <span class="title">{{ name }}</span>
      </div>
      <span class="value">{{ value }} %</span>
    </div>
    <div class="range-bar">
      <div class="range" :style="{ backgroundColor: color, width: value + '%' }"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BalanceItem',
  props: {
    icon: String,
    name: String,
    value: Number,
    color: String
  }
}
</script>

<style scoped>
.balance-item {
  width: 100%;
  height: 60px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  align-items: center;
  margin-top: 10px;
}

.text-container {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  margin-left: 20px;
  text-align: center;
}
.title-container {
  display: flex;
  height: 100%;
  justify-content: center;
  align-items: center;
}
.title,
.value {
  font-family: 'Poppins';
  font-size: 14px;
  font-weight: 500;
  line-height: 21px;
  text-align: left;
  color: #000000;
  margin-top: -10px;
}

.range-bar {
  width: 100%;
  height: 10px;
  border-radius: 5px;
  background-color: #d9d9d9;
}
.range {
  height: 100%;
  border-radius: 5px;
}
</style>
