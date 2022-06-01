<template>
 <header class="menu-superior">
    <div class="menu-esquerdo">
      <span> Home </span>
      <span>|</span>
      <span> Times </span>
      <span>|</span>
      <span> Jogadores </span>
    </div>

    <div class="menu-direito">
      <span>Sair</span>
    </div>
  </header>
  <RouterView />
</template>

<style>
@import "@/assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  /* padding: 2rem; */
  height: 100vh;

  font-weight: normal;
}
header,
footer {
  background-color: green;
  color: Black;
  font-size: 1.3rem;
  height: 15%;
  display: flex;
  align-items: center;
  padding-left: 2rem;
}

main {
  height: 70%;
}
header span {
  padding: 0 20px;
}

header.menu-superior {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
