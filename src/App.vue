<script setup>
import HelloWorld from './components/HelloWorld.vue';
import Odissey from './components/Odissey.vue';

</script>

<template>
  <Odissey></Odissey>

  <h1 class="Main_Title">THIS IS MY ODISSEY FONT</h1>
</template>

<style scoped>

@font-face {
  font-family: OdisseyFont;
  src: url('./static/fonts/HomepageBaukasten-Bold.ttf');
}

.Main_Title {
  color: #2F5E8D;
  font-family: OdisseyFont, sans-serif;
}


</style>
