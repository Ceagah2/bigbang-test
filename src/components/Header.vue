<template>
  <div class="header-container">
    <div class="logo-container">
      <img src="../assets/logo.png" class="logo-image" />
    </div>
    <nav class="navigation">
      <ul class="nav-menu">
        <li class="nav-item active">Dashboard</li>
        <li class="nav-item">Pagamentos</li>
        <li class="nav-item">Invoices</li>
        <li class="nav-item">Insights</li>
      </ul>
    </nav>
    <div class="icon-container">
      <i class="fa-regular fa-bell fa-2xl"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style scoped>
.header-container {
  width: 100vw;
  height: 60px;
  background: #202027;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  padding: 0 30px 0 30px;
  margin-bottom: 20px;
}
.logo-container {
}
.logo-image {
  width: 100%;
  height: 100%;
}
.logo-image:hover {
  cursor: pointer;
}
.navigation {
  height: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.nav-menu {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  color: white;
}
.active {
  background: #ff6969;
}
.nav-item {
  padding: 10px 20px;
  list-style: none;
  margin: 10px;
  font-family: 'Poppins', sans-serif;
  min-width: 150px;
  text-align: center;
}
.nav-item:hover {
  cursor: pointer;
}
.icon-container {
  color: white;
}
</style>
