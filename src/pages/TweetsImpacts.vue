<template>
  <div>
    <second-header selected="choose-person" />
    <div class="main">
      <div class="central-text-box">
        <h1 class="title">{{person.name}} tweets impacts</h1>
        <div class="horizontal-band"></div>
      </div>

      <div class="photo" :style="`background-image: url(${person.photoUrl});`" />
      <tabs :person="person"></tabs>
    </div>
  </div>
</template>
<script>
import influentialPeople from "@/assets/influentialPeople.json";
import Tabs from "../components/CustomTabs";
import SecondHeader from "../components/SecondHeader";

export default {
  components: {
    Tabs,
    SecondHeader,
  },
  data() {
    return {
      person: {},
    };
  },
  created() {
    this.person = influentialPeople.find(
      (x) => x.name === this.$route.params.name
    );
  },
};
</script>
<style scoped>
.nav-bar {
  background-color: var(--color-green);
}
.button {
  color: white;
}
.button::before {
  background-color: white;
}
.main {
  padding: 2em 0;
}
.title {
  color: var(--color-green);
  font-size: 2em;
  word-spacing: normal;
}
.horizontal-band {
  background-color: var(--color-green);
}
.subtitle {
  color: var(--color-green);
}
.photo {
  border-radius: 50%;
  height: 10em;
  width: 10em;
  background-size: cover;
  background-repeat: no-repeat;
  margin-right: 10px;
  border: 1px var(--color-green) solid;
  margin: 2em auto;
}
.charts-container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 100%;
  margin-top: 1em;
}
.graphs-container {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.section-title {
  font-size: 1.3em;
  color: var(--color-green);
  text-align: center;
}
.vertical-bar {
  height: 100%;
  width: 1px;
  background-color: var(--color-green);
}
</style>