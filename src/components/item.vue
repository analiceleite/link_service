<template>
  <div class="card">
    <a :href="item.href">
      <img :src="item.img" alt="Icone do servico" />
      <span>{{ item.titulo }}</span>
    </a>
  </div>
</template>

<script>
export default {
  props: ["item"],
};
</script>

<style scoped>
div {
  margin: 20px 50px 20px 50px;
  display: block;
  width: 100px;
}
img {
  width: 80px;
}
span {
  font-weight: 900;
}

.card {
    min-width: 120px;
    border: 1px solid grey;
    border-radius: 5%;
    opacity: .9;
    box-shadow: 0 0 2em grey;
    transition: box-shadow 0.5s;
}

.card:hover {
    box-shadow: 0 0 3em grey;
    opacity: 1;
}
</style>
