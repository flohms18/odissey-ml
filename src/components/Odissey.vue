<script setup>
import { onMounted, ref } from 'vue';
import Footer from './Footer.vue';
import Header from './Header.vue';

const titleRef = ref(null);
const subtitleRef = ref(null);

onMounted(() => {
  titleRef.value.textContent = titleRef.value.textContent.toUpperCase();
  subtitleRef.value.textContent = "COMING SOON..."
});
</script>

<template>
    <div class="d-flex flex-column min-vh-100">
        <Header></Header>
        <div class="d-flex flex-column justify-content-center align-items-center flex-grow-1 text-center">
            <h1 id="main-title" ref="titleRef">The Odissey of Machine Learning</h1>
            <h4 id="main-subtitle" class="mt-2" ref="subtitleRef">Coming Soon</h4>
        </div>
        <Footer></Footer>
    </div>
</template>

<style scoped>

:root {
  --dark-color : #0D0D0D;
  --blue-color: #2F5E8D;
  --red-color : #ce2127;
}

@keyframes fadeSlideUp {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

#main-title {
    color: var(--blue-color);
    font-family: OdisseyFont, sans-serif;
    animation: fadeSlideUp 0.9s cubic-bezier(0.22, 1, 0.36, 1) forwards;
}

#main-subtitle {
    color: var(--red-color);
    font-family: OdisseyFont, sans-serif;
    opacity: 0;
    animation: fadeSlideUp 0.9s cubic-bezier(0.22, 1, 0.36, 1) 0.45s forwards;
}

</style>

