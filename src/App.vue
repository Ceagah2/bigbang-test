<template>
  <div class="container">
    <AppHeader />
    <CashContainer />
    <div class="transactions-container">
      <TransactionsContainer />
      <BalanceContainer />
    </div>
  </div>
</template>

<script>
import BalanceContainer from './components/BalanceContainer.vue'
import CashContainer from './components/CashContainer.vue'
import AppHeader from './components/Header.vue'
import TransactionsContainer from './components/Transactions.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    CashContainer,
    TransactionsContainer,
    BalanceContainer
  }
}
</script>

<style>
.container {
  width: 100vw;
  height: 100%;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background: white;
  padding-top: 20px;
}
.transactions-container {
  width: 80%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
}
</style>
