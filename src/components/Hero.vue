<script setup></script>

<template>
  <section class="hero">
    <img
      class="picture"
      src="../assets/fotografo.png"
      alt="Foto de alguém tirando foto"
    />
    <div class="texto">
      <h1>Onde a paisagem vira <span class="destaque">inspiração</span>.</h1>
      <p class="desc">
        Explore paisagens, cores e luzes que inspiram novas histórias através da
        fotografia.
      </p>
    </div>
  </section>
</template>

<style scoped lang="scss">
.hero {
  display: flex;
  flex-direction: column;
  padding: 1.5rem;
}

.picture {
  padding: 2rem 4rem;
}

h1 {
  color: #262626;
  font-size: 60px;
  text-align: center;

  .destaque {
    color: #e1306c;
    font-size: 80px;
  }
}

.desc {
  color: #262626;
  text-align: center;
  font-size: 19px;
  padding: 1rem 0;
}

@media (min-width: 768px) {
  .hero {
    flex-direction: row-reverse;
    align-items: center;
  }

  .picture {
    width: 50%;
  }

  .texto {
    width: 50%;
  }
}
</style>
