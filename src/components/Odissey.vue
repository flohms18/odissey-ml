<script setup>
import { onMounted } from 'vue';
import Footer from './Footer.vue';
import Header from './Header.vue';

onMounted(() => {
  const OdisseyTitle = document.getElementById('main-title');
  OdisseyTitle.textContent = OdisseyTitle.textContent.toUpperCase()
});
</script>

<template>
    <Header></Header>
    <div class="d-flex">
        <h1 id="main-title">The odissey of Machine Learning</h1>
    </div>
    <Footer></Footer>
</template>

<style scoped>

:root {
  --dark-color : #0D0D0D; 
  --blue-color: #2F5E8D;
  --red-color : #ce2127;
}

#main-title {
    color: var(--blue-color);
    font-family: OdisseyFont, sans-serif;

}

</style>

