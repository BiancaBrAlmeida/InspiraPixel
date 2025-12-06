<script setup>
import { Icon } from "@iconify/vue";
defineProps(["imagem"]);
</script>

<template>
  <div class="card">
    <button>
      <Icon icon="mdi:heart" width="30" height="30" style="color: #fff" />
    </button>
    <img :src="imagem" alt="" />
  </div>
</template>

<style scoped lang="scss">
.card {
  width: 16rem;
  height: 25rem;
  position: relative;
  margin: 2rem;

  img {
    border-radius: 10px;
    width: 100%;
    height: 100%;
    object-fit: cover;
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
</style>
