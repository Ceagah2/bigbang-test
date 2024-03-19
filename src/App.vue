<template>
  <div class="container">
    <AppHeader />
    <CashContainer />
    <div class="transactions-container"></div>
  </div>
</template>

<script>
import AppHeader from './components/Header.vue'
import CashContainer from './components/CashContainer.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    CashContainer
  }
}
</script>

<style>
.container {
  width: 100vw;
  height: 100vw;
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
