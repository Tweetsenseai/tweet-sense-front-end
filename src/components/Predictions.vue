<template>
  <div class="graphs-container">
    <div v-for="(prediction, index) in person.predictionsCharts" :key="index" class="graph">
      <p class="graph-title">{{prediction.title}}</p>
      <custom-iframe :link="prediction.link" />
    </div>
  </div>
</template>
<script>
import CustomIframe from "./CustomIframe";

export default {
  props: ["person"],
  components: {
    CustomIframe,
  },
};
</script>
<style>
.graphs-container {
  margin: 2em 0;
}
.graph-title {
  text-align: center;
}
.graphs-container > * {
  margin-bottom: 4em;
}
@media only screen and (max-width: 600px) {
  .graphs-container {
    width: 100%;
    overflow: scroll;
  }
}
</style>