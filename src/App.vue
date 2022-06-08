<script setup>
import HeaderComp from "@/components/template/HeaderComp.vue";
import RodapéComp from "./components/template/RodapéComp.vue";
</script>
<template>
  <HeaderComp />
  <main>
    <RouterView />
  </main>
  <RodapéComp />
</template>

<style>
@import "@/assets/base.css";
@import "@/assets/style.css";

#app {
  /* max-width: 1280px; */
  margin: 0 auto;
  /* padding: 2rem; */
  height: 100vh;

  font-weight: normal;
}
header,
footer {
  background: rgb(63, 94, 251);
  background: radial-gradient(
    circle,
    rgba(63, 94, 251, 1) 0%,
    rgba(252, 70, 107, 1) 100%
  );
  color: rgb(51, 44, 44);
  font-size: 1.3rem;
  height: 15%;
  display: flex;
  align-items: center;
  padding-left: 2rem;
}
a {
  color: rgb(70, 40, 40);
  text-decoration: none;
}
main {
  height: 70%;
}
</style>
