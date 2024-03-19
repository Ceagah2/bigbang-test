<template>
  <div class="transaction-item">
    <div class="icon-container" :style="{ backgroundColor: color }">
      <img src="../assets/shop.png" alt="shop icon" />
    </div>
    <div class="transaction-details">
      <span class="transaction-name">{{ name }}</span>
      <span class="transaction-value">R${{ value }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TransactionItem',
  props: {
    color: String,
    name: String,
    value: String
  }
}
</script>

<style scoped>
.transaction-item {
  width: 80%;
  height: 70px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  border-top: 1px solid #b3b3b3;
}
.icon-container {
  width: 40px;
  height: 40px;
  border-radius: 5px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.icon {
}
.transaction-details {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 0 10px;
}
.transaction-name {
  font-family: 'Poppins';
  font-size: 14px;
  font-weight: 500;
  line-height: 21px;
  text-align: left;
  color: #202027;
}
.transaction-value {
  font-family: 'Poppins';
  font-size: 14px;
  font-weight: 500;
  line-height: 21px;
  text-align: right;
  color: #000000;
}
</style>
