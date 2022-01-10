<template>
  <div class="card-wrapper">
    <h1 class="title">Angaben zu Ihrer Maschine</h1>
    <section class="main-info__grid">
      <img class="main-info__img" :src="image" alt="asset image" />
      <span class="main-info__header">
        <div class="asset-name">Hako - Sonstige Reinigung</div>
        <h3 class="asset-type">Superpro Battery 700 Advanced</h3>
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

    <section class="checks-info">
      <div class="maintenance">
        <span class="maintenance__title subtitle">Wartung</span>
        <span>Letzte Wartung </span>
        <span class="date">29.09.2021</span>
        <span>Nächste Wartung</span>
        <span class="date">29.09.2022</span>
      </div>
      <hr />
      <div class="machine-check">
        <span class="machine-check__title subtitle"
          >Electric AC/DC 123-54455 prüfung</span
        >
        <span>Letzte Prüfung</span>
        <span class="date">29.09.2020</span>
        <span>Nächste Prüfung</span>
        <span class="date">29.09.2021</span>
      </div>
      <hr />
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
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700&display=swap");

h3 {
  margin: 0;
}
.card-wrapper {
  overflow-x: hidden;
  color: #484037;
  font-family: "Open Sans", sans-serif;
  font-weight: 400;
  font-size: calc(15px + (3 + 3 * 0.9) * ((100vw - 375px) / 768));
  line-height: 120%;
  max-width: 768px;
  margin: 0 auto;
}

h1.title {
  margin: 16px 0 12px 19px;
  font-weight: 700;
  font-size: calc(24px + (10 + 11 * 0.87) * ((100vw - 375px) / 768));
  line-height: 136%;
  color: #83817F;
  text-align: left;
}

.main-info__grid {
  background-color: #F9F9F9;
  padding: 16px 16px 19px;
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
  font-weight: 700;
  margin-bottom: 4px;
}

.asset-type {
  font-weight: 700;
  font-size: calc(20px + (7.6 + 9 * 0.9) * ((100vw - 375px) / 768));
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

.checks-info {
  padding: 26px 16px 4px 16px;
}

.maintenance,
.machine-check {
  padding-bottom: 4px;
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-gap: 8px;
}

.machine-check {
  padding-top: 4px;
}

.subtitle {
  grid-column: span 2;
  padding-bottom: 4px;
  font-weight: 700;
  font-size: calc(17px + (5 + 6 * 0.8) * ((100vw - 375px) / 768));
  line-height: 106%;
}

.date {
  justify-self: right;
}

@media only screen and (min-width: 600px) {
  h1.title {
    margin-top: 32px;
    margin-left: 32px;
  }

  .main-info__grid {
    padding: 32px;
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

  .checks-info {
    padding: 32px;
  }
}
</style>