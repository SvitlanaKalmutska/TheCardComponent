<template>
  <div class="card-wrapper">
    <h1 class="title">Angaben zu Ihrer Maschine</h1>
    <section class="main-info__grid">
      <img class="main-info__img" :src="image" alt="asset image" />
      <span class="main-info__header">
        <div class="asset-name">Hako - Sonstige Reinigung</div>
        <h3 class="asset-sign">Superpro Battery 700 Advanced</h3>
      </span>
      <span class="key">Serial</span>
      <span>312aa</span>
      <hr />
      <span class="key">Objekt</span>
      <span>Hotel ABC - 22555566544</span>
      <hr />
      <span class="key">Adresse</span>
      <span>Praterstraße 1, 1020 Wien, Österreich</span>
    </section>
  </div>
</template>

<script>
import image from "../assets/asset.png";

export default {
  name: "TheCard",
  props: {
    msg: String,
  },
  data() {
    return {
      image,
    };
  },
};
</script>

<style scoped>
h1.title {
  margin: 16px 0 12px;
  font-family: "Open Sans", sans-serif;
  font-weight: 700;
  font-size: calc(24px + (10 + 11 * 0.87) * ((100vw - 375px) / 768));
  line-height: 136%;
  /* font-size: 24px; */
  /* line-height: 32.68px; */
  color: #83817F;
  text-align: center;
}

.main-info__grid {
  background-color: #F9F9F9;
  padding: 16px 8px;
  display: grid;
  grid-template-columns: 1fr 3.5fr;
  column-gap: 1rem;
}

.main-info__img {
  max-width: 100%;
  object-fit: contain;
  border-radius: 12px;
  margin-bottom: 16px;
}

.main-info__header {
  margin-bottom: 20px;
}

.asset-name {
  font-weight: 500;
  margin-bottom: 4px;
}

.asset-sign {
  font-weight: 700;
  font-size: calc(20px + (7.6 + 8 * 0.9) * ((100vw - 375px) / 768));
  line-height: 120%;
}

hr {
  border: 0;
  background: #F3F1F0;
  height: 1px;
  grid-column: span 2;
  margin: 8px 0;
}

.key {
  font-weight: 700;
}

@media only screen and (min-width: 600px) {
  h1 {
    margin-top: 32px;
  }

  .main-info__grid {
    padding: 32px 32px;
    column-gap: 1.75rem;
  }

  .asset-name {
    margin-bottom: 8px;
  }

  .main-info__img {
    margin-bottom: 24px;
  }

  hr {
    margin: 16px 0;
  }
}
</style>