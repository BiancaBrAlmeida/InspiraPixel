<script setup>
import { Icon } from "@iconify/vue";
import { ref } from "vue";
defineProps(["imagem"]);

const favorito = ref(false);
const toggleFavorito = () => {
  favorito.value = !favorito.value;
};
</script>

<template>
  <div class="card">
    <button
      :class="['iconNormal', { iconClicou: favorito }]"
      @click="toggleFavorito"
    >
      <Icon icon="mdi:heart" width="30" height="30" />
    </button>
    <img :src="imagem" alt="Imagem aleatória" />
  </div>
</template>

<style scoped lang="scss">
.card {
  width: 16rem;
  height: 25rem;
  position: relative;
  margin: 2rem;
  // border-radius: 10px;
  // box-shadow: 1px 1px 10px black;

  img {
    border-radius: 10px;
    width: 100%;
    height: 100%;
    object-fit: cover;
    box-shadow: 1px 1px 10px #e7a4ba;
  }

  button {
    position: absolute;
    right: 10px;
    top: 10px;
    cursor: pointer;
    background-color: transparent;
    border: none;
  }
}

.iconNormal :deep(svg) {
  color: #ffffff;
  transition: color 0.3s ease;
  filter: drop-shadow(0px 1px 10px #525252);

  &:hover {
    color: #e7a4ba;
  }
}

.iconClicou :deep(svg) {
  color: #e1306c;
}
</style>
