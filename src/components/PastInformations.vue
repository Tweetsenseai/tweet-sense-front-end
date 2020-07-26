<template>
  <div class="graphs-container">
    <div v-for="(pastChart, index) in person.pastCharts" :key="index" class="graph">
      <p class="graph-title">{{pastChart.title}}</p>
      <custom-iframe :link="pastChart.link" />
    </div>
  </div>
</template>
<script>
import CustomIframe from "./CustomIframe";
export default {
  components: {
    CustomIframe,
  },
  props: ["person"],
};
</script>
<style>
@media only screen and (max-width: 600px) {
  iframe {
    overflow: scroll;
  }
  .graph {
    width: 100%;
  }
}
</style>