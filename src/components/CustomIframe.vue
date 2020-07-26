<template>
  <iframe
    frameborder="0"
    allowtransparency="true"
    allowfullscreen="true"
    title="Data Visualization"
    marginheight="0"
    marginwidth="0"
    scrolling="no"
    :src="link + '&:showVizHome=no&embed=true'"
  ></iframe>
</template>

<script>
export default {
  props: ["link"],
};
</script>
<style>
iframe {
  display: block;
  width: 1020px;
  height: 1196px;
  visibility: visible;
}
</style>