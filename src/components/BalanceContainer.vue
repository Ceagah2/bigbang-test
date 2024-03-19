<template>
  <div class="balance-container">
    <div class="container-header">
      <div class="title-container">
        <img class="icon" src="../assets/balance.png" alt="transactions icon" />
        <h3 class="title">Análise geral</h3>
        <h4 class="subtitle">últimos 7 dias</h4>
      </div>
      <span class="menu">Ver todas</span>
    </div>
    <div class="transactions-container">
      <div class="balance">
        <div class="balance-value-container">
          <span class="balance-title">Ganhos</span>
          <span class="balance-value">R$ {{ balance.incoming }}</span>
        </div>
        <div class="balance-value-container">
          <span class="balance-title">Saidas</span>
          <span class="balance-value">R$ {{ balance.outgoing }}</span>
        </div>
      </div>
      <BalanceItem
        v-for="transaction in transactions"
        :key="transaction.id"
        :name="transaction.name"
        :value="transaction.value"
        :color="transaction.color"
        :icon="transaction.icon"
      />
    </div>
  </div>
</template>

<script>
import { balance, transactions } from '../constants/mock'
import BalanceItem from './BalanceItem.vue'
export default {
  name: 'BalanceContainer',
  components: {
    BalanceItem
  },
  data() {
    return {
      balance,
      transactions
    }
  },
  mounted() {
    console.log(transactions)
  }
}
</script>

<style scoped>
.balance-container {
  width: 90%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
.container-header {
  width: 80%;
  height: 60px;
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
  width: 80%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
.balance {
  width: 100%;
  height: 85px;
  border-bottom: 1px solid #b3b3b3;
  border-top: 1px solid #b3b3b3;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.balance-value-container {
  width: 20%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  text-align: center;
}
.balance-value {
  font-family: 'Poppins';
  font-size: 20px;
  font-weight: 500;
  line-height: 30px;
  text-align: left;
  color: #000000;
}
.balance-title {
  font-family: 'Poppins';
  font-size: 14px;
  font-weight: 500;
  line-height: 21px;
  text-align: left;
  color: #000000;
}
</style>
