<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import RandomDinguerie from "./components/RandomDinguerie.vue";
</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld msg="Random dinguerie" />
    </div>
  </header>

  <main id="main">
    <div class="dinguerie">
      <RandomDinguerie />
    </div>
  </main>
</template>

<style scoped>
header {
  margin-top:auto;
  line-height: 1;
  height: 250px;
}
header .wrapper {
  position: fixed;
  top: 0px;
  left: 0px;
  width: 100%;
  z-index: 1000;
}
</style>
