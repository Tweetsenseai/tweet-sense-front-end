<template>
  <div class="main-container">
    <first-header selected="about" />
    <div class="about-main">
      <img class="detail left" src="@/assets/green-square.svg" alt="detail" />
      <img class="detail right" src="@/assets/green-square.svg" alt="detail" />
      <div class="central-text-box">
        <h1 class="title">ABOUT US</h1>
        <div class="horizontal-band"></div>
        <h4
          class="subtitle"
        >Sentiment analysis of the tweets of influential people, the resultant emotional sentiments and their impacts on socio-economic spheres</h4>
      </div>
    </div>
  </div>
</template>
<script>
import FirstHeader from "../components/FirstHeader";
export default {
  components: {
    FirstHeader,
  },
};
</script>
<style scoped>
.nav-bar {
  margin-bottom: 0;
}
.main-container {
  height: 100vh;
  overflow: hidden;
}
.about-main {
  height: 100%;
  width: 100vw;
  display: flex;
  background-color: var(--color-yellow);
  flex-direction: column;
  position: relative;
  overflow: hidden;
}
.title {
  word-spacing: normal;
  color: var(--color-green);
}
.subtitle {
  font-size: 1.2em;
  padding: 0 10px;
  color: var(--color-green);
  text-align: center;
}
.horizontal-band {
  background-color: var(--color-green);
}
</style>