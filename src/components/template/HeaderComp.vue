<template>
  <header class="menu-superior">
    <div class="menu-esquerdo">
      <span> <RouterLink to="/">Home</RouterLink></span>
      <span>||</span>
      <span> <RouterLink to="/times">Times</RouterLink> </span>
      <span>||</span>
      <span> <RouterLink to="/jogadores">Jogadores</RouterLink> </span>
    <div>
      <h1 class="rainbo">bom diaaa</h1>
    </div>  
    </div>
    <div class="menu-direito">
      <nav>
        <span> | Sair |</span>
      </nav>
    </div>
  </header>
</template >
<style>
header span {
  padding: 0 20px;
}

header.menu-superior {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.rainbo {
  text-decoration: wavy;
  text-align: center;
  font-size: 32px;
  letter-spacing: 2px;
  animation: colorRotate 6s linear 0s infinite;
}

@keyframes colorRotate {
  from {
    color: #373793;
  }
  10% {
    color: #006aff;
  }
  50% {
    color: #00ff00;
  }
  75% {
    color: #fc0f2b;
  }
  100% {
    color: #6666ff;
  }
}

</style>
