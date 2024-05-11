<script setup>
import item from "./components/item.vue";
</script>

<script>
import dados from "./data/services.json";
export default {
  data() {
    return {
      services: null,
    };
  },
  mounted() {
    this.services = dados;
    console.log(dados);
  },
};
</script>

<template>
  <div>
    <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    <h1>Seja bem vindo(a)!</h1>
    <hr />
    <div class="items">
      <item v-for="(service, index) in services" :key="index" :item="service" />
    </div>
  </div>
</template>

<style scoped>

.items {
  display: flex;
  justify-content: center;
  /* Faz com que, ao diminuir a tela os itens se adequem */
  flex-wrap: wrap;
}

.logo {
  width: 100px;
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #ffffffaa);
}
</style>
