<template>
  <nav class="nav-bar">
    <router-link :to="{name: 'home'}" class="tab__link">
      <div class="button" :class="{selected: selected==='home'}">Home</div>
    </router-link>
    <router-link :to="{name: 'about'}" class="tab__link">
      <div class="button" :class="{selected: selected==='about'}">About</div>
    </router-link>
    <router-link :to="{name: 'choose-person'}" class="tab__link">
      <div class="button" :class="{selected: selected==='choose-person'}">Tweetlytics</div>
    </router-link>
  </nav>
</template>
<script>
export default {
  props: ["selected"],
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
</style>