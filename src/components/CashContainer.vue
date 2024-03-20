<template>
  <div class="cash-container">
    <div class="container-header">
      <div class="header-text-container">
        <div class="value-container">
          <h3>Saldo total</h3>
          <div class="values-container">
            <span class="value">R$ {{ total.toFixed(2) }}</span>
            <span style="color: yellow; margin: 0 10px">
              <i class="fa-solid fa-bolt fa-2xl"></i>
            </span>
            <span style="color: white">rendendo 124%</span>
          </div>
        </div>
        <div class="buttons-container">
          <button class="send-button">
            <i class="fa-brands fa-airbnb fa-l" style="transform: rotate(45deg)"></i>
            Enviar dinheiro
          </button>
          <button class="add-button">
            <i class="fa-solid fa-plus fa-l"></i>
          </button>
        </div>
      </div>
    </div>
    <div class="money-container">
      <div class="cards-title">
        <img src="../assets/bubble.png" alt="bubbles" />
        <h3 class="title">Painel de estatísticas</h3>
        <span class="subtitle">últimos 7 dias</span>
      </div>
      <div class="cards-container">
        <ValueCard title="Conta Pj" :value="pj" />
        <ValueCard title="Recebimentos" :value="incoming" />
        <ValueCard title="Lucro" :value="profit" />
      </div>
    </div>
  </div>
</template>

<script>
import { values } from '../constants/mock'
import ValueCard from './atoms/Card.vue'

export default {
  name: 'CashContainer',
  components: {
    ValueCard
  },
  data() {
    return {
      total: values.total,
      pj: values.pj,
      incoming: values.incoming,
      profit: values.profit
    }
  }
}
</script>

<style scope>
.cash-container {
  width: 100%;
  height: 50vh;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  margin-top: 0 auto;
  padding-top: 20px;
  background: linear-gradient(#202027 60%, white 60%);
}
.container-header {
  width: 80%;
  height: 20%;
  display: flex;
  justify-content: flex-start;
  align-items: center;
}
.header-text-container {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
  margin-left: 20px;
}

.value-container {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  text-align: left;
}
.value-container > h3 {
  font-family: 'Poppins', sans-serif;
  font-size: 20px;
  font-weight: 500;
  line-height: 30px;
  text-align: center;
  color: white;
}
.values-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.value {
  font-family: 'Poppins', sans-serif;
  font-size: 36px;
  font-weight: 500;
  line-height: 54px;
  text-align: left;
  color: white;
}
.buttons-container {
  width: 40%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-end;
}
.send-button {
  width: 254px;
  height: 37px;
  background: #7986fe;
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  font-weight: 500;
  line-height: 21px;
  text-align: center;
  color: white;
  border: none;
}
.add-button {
  width: 56px;
  height: 37px;
  background: #7986fe;
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  font-weight: 500;
  line-height: 21px;
  text-align: center;
  color: white;
  border: none;
}
button:hover {
  cursor: pointer;
  opacity: 0.8;
}
.cards-title {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  padding-left: 20px;
}
.title {
  font-family: 'Poppins', sans-serif;
  font-size: 20px;
  font-weight: 500;
  line-height: 30px;
  text-align: center;
  color: white;
  margin-left: 10px;
}
.subtitle {
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  font-weight: 500;
  text-align: center;
  color: #a3a3a3;
  margin: 10px 20px;
}
.money-container {
  width: 80%;
  height: 80%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
.cards-container {
  width: 80%;
  height: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  margin-top: 20px;
}
</style>
