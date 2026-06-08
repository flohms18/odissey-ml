<script setup>
import HelloWorld from './components/HelloWorld.vue';
import Odissey from './components/Odissey.vue';

import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

</script>

<template>
  <Odissey></Odissey>

  <section>
    <div class="d-flex bg-danger flex-row">
      <div class="p-2">Flex item 1</div>
      <div class="p-2">Flex item 2</div>
      <div class="p-2">Flex item 3</div>
    </div>
  </section>
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
