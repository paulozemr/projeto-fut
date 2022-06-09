<template>
  <main id="shadowBox">
    <h1 class="rainbow">Bem Vindo ao meu Site de Futebol</h1>
    <h3>Site criado por: Paulo José Ramos Zem</h3>
    <img 
    src="https://c.tenor.com/aaEMtGfZFbkAAAAC/rat-spinning.gif"
    alt=""
    />
  </main>
</template>
<style scoped>
#shadowBox {

  align-items: center;
  text-align: center;
}
.rainbow {
  text-align: center;
  font-size: 32px;
  animation: colorRotate 6s linear 0s infinite;
}

@keyframes colorRotate {
  from {
    color: #6666ff;
  }
  10% {
    color: #0099ff;
  }
  50% {
    color: #00ff00;
  }
  75% {
    color: #ff3399;
  }
  100% {
    color: #6666ff;
  }
}
</style>


