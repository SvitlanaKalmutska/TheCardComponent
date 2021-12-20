<template>
  <div class="card-wrapper">
    <h1 class="title">Angaben zu Ihrer Maschine</h1>
    <section class="main-info">
      <div class="container">
        <div class="main-info__row">
          <span class="main-info__img">
            <img :src="image" alt="asset image" />
          </span>
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
        </div>
      </div>
    </section>

    <!-- <section class="extra-info">
      <div class="container">
        <div class="extra-info__wrapper">
          <div class="maintenance">
            <span class="maintenance__title subtitle">Wartung</span>
            <span>Letzte Wartung </span>
            <span>29.09.2021</span>
            <span>Nächste Wartung</span>
            <span>29.09.2022</span>
          </div>
          <div class="machine-check">
            <span class="machine-check__title subtitle"
              >Electric AC/DC 123-54455 prüfung</span
            >
            <span class="machine-check__link">
              <a href="#">Due</a>
            </span>
            <span>Letzte Prüfung: </span>
            <span>29.09.2020</span>
            <span>Nächste Prüfung:</span>
            <span>29.09.2021</span>
          </div>          
        </div>
      </div>
    </section>
    <section class="buttons"></section> -->
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
.main-info {
  background-color: #F9F9F9;
}
.main-info__row {
  padding: 16px 0;
  display: grid;
  grid-template-columns: 1fr 3.5fr;
  justify-items: left;
  align-items: center;
  column-gap: 1rem;
}
.main-info__img {
  width: 100%;
  height: auto;
  border-radius: 12px;
  overflow: hidden;
  margin-bottom: 16px;
  align-self: self-start;
}
.main-info__img img {
  max-width: 100%;
  object-fit: contain;
  border-radius: 12px;
}
.main-info__header {
  margin-bottom: 20px;
  align-self: start;
}
.asset-name {
  font-weight: 500;
  margin-bottom: 4px;
}
.asset-sign {
  font-weight: 700;
  /* font-size: 20px; */
  font-size: calc(20px + (7.6 + 8 * 0.9) * ((100vw - 375px) / 768));
  /* line-height: 24px; */
  line-height: 120%;
}
hr {
  border: 0;
  background: #F3F1F0;
  height: 1px;
  width: 100%;
  grid-column: span 2;
  margin: 8px 0;
}
.key {
  font-weight: 700;
}
/* .machine-check,
.maintenance {
  display: grid;
  grid-template-columns: 1fr 1fr;
  justify-items: left;
  align-items: center;
  column-gap: 1rem;
  row-gap: 1rem;
}
.maintenance {
  border-top: 1px solid #F3F1F0;
} */

@media only screen and (min-width: 600px) {
  h1 {
    margin-top: 32px;
  }
  .container {
    padding: 0 32px;
  }
  .main-info__row {
    padding: 32px 0;
    column-gap: 1.75rem;
  }
  .asset-name {
    margin-bottom: 8px;
  }
  .main-info__img {
    margin-bottom: 24px;
    align-self: self-start;
  }
  hr {
    margin: 16px 0;
  }
}
</style>
