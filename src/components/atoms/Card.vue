<template>
  <div class="card-container">
    <span class="card-title">{{ title }}</span>
    <span class="card-value">R$ {{ value }}</span>
    <div class="buttons-container">
      <button class="details-button">Ver mais detalhes</button>
      <button class="details-button-responsive">Detalhes</button>
      <button class="menu-button">
        <i class="fa-solid fa-bars"></i>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ValueCard',
  props: {
    title: String,
    value: String
  }
}
</script>

<style scoped>
.card-container {
  width: 350px;
  height: 220px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  padding: 20px;
  background: white;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.25);
}
.card-title {
  font-family: 'Poppins', sans-serif;
  font-size: 16px;
  font-weight: 500;
  text-align: left;
  color: #000000;
}
.card-value {
  font-family: 'Poppins', sans-serif;
  font-size: 24px;
  font-weight: 500;
  line-height: 36px;
  text-align: left;
  color: #000000;
}
.buttons-container {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.details-button {
  width: 70%;
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  font-weight: 400;
  line-height: 21px;
  text-align: left;
  color: #686868;
  border: 1px solid #747474;
  padding: 10px;
  text-align: center;
}
.details-button-responsive {
  display: none;
  width: 70%;
  font-family: 'Poppins', sans-serif;
  font-size: 14px;
  font-weight: 400;
  line-height: 21px;
  text-align: left;
  color: #686868;
  border: 1px solid #747474;
  padding: 10px;
  text-align: center;
}
.menu-button {
  width: 50px;
  height: 35px;
  border: 1px solid #747474;
}

@media screen and (max-width: 1350px) {
  .card-container {
    width: 300px;
  }
}

@media screen and (max-width: 1150px) {
  .card-container {
    width: 250px;
  }
  .menu-button {
    height: 65px;
  }
}
@media screen and (max-width: 950px) {
  .card-container {
    width: 220px;
  }
  .details-button {
    display: none;
  }
  .details-button-responsive {
    display: block;
    width: 60%;
  }
  .menu-button {
    height: 45px;
  }
}
</style>
