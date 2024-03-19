<template>
  <div class="container">
    <AppHeader />
    <CashContainer />
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
  background-color: #202027;
  padding-top: 20px;
}
</style>
