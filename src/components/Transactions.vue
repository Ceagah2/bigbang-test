<template>
  <div class="transactions-container">
    <div class="container-header">
      <div class="title-container">
        <img class="icon" src="../assets/transactions.png" alt="transactions icon" />
        <h3 class="title">Transações recentes</h3>
        <h4 class="subtitle">últimos 7 dias</h4>
      </div>
      <span class="menu">Ver todas</span>
    </div>
    <div class="transactions-container">
      <TransactionItem
        v-for="location in locations"
        :key="location.id"
        :color="location.color"
        :name="location.name"
        :value="location.value"
      />
    </div>
  </div>
</template>

<script>
import { locations } from '../constants/mock'
import TransactionItem from './atoms/TransactionItem.vue'

export default {
  name: 'TransactionsContainer',
  components: {
    TransactionItem
  },
  data() {
    return {
      locations
    }
  }
}
</script>

<style scoped>
.transactions-container {
  width: 40%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
.container-header {
  width: 80%;
  height: 70px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.icon {
}
.title-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  text-align: center;
}
.title {
  font-family: 'Poppins';
  font-size: 20px;
  font-weight: 500;
  line-height: 30px;
  text-align: left;
  color: #202027;
}
.subtitle {
  font-family: 'Poppins';
  font-size: 14px;
  font-weight: 500;
  line-height: 21px;
  text-align: left;
  color: #a3a3a3;
}
.menu {
  font-family: 'Poppins';
  font-size: 14px;
  font-weight: 500;
  line-height: 21px;
  color: #7986fe;
}
.menu:hover {
  cursor: pointer;
}

.transactions-container {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
</style>
