<template>
  <TheCard />
</template>

<script>
import TheCard from "./components/TheCard";

export default {
  name: "App",
  components: {
    TheCard,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@700&family=Roboto:wght@700&display=swap");

body {
  margin: 0;
  box-sizing: border-box;
  overflow-x: hidden;
  color: #484037;
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  font-size: calc(15px + (3 + 3 * 0.9) * ((100vw - 375px) / 768));
  line-height: 120%;
}
h3 {
  margin: 0;
}
.container {
  margin: 0 auto;
  padding: 0 16px;
}
</style>
