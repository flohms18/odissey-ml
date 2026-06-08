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
            <div class="container px-4 px-md-5">
                <h1 id="main-title" ref="titleRef">The Odissey of Machine Learning</h1>
                <h4 id="main-subtitle" class="mt-2 mt-md-3" ref="subtitleRef">Coming Soon</h4>
            </div>
        </div>
        <Footer></Footer>
    </div>
</template>

<style scoped>

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
    font-size: 1.8rem;
    animation: fadeSlideUp 0.9s cubic-bezier(0.22, 1, 0.36, 1) forwards;
}

#main-subtitle {
    color: var(--red-color);
    font-family: OdisseyFont, sans-serif;
    font-size: 1rem;
    opacity: 0;
    animation: fadeSlideUp 0.9s cubic-bezier(0.22, 1, 0.36, 1) 0.45s forwards;
}

/* Bootstrap sm breakpoint: 576px */
@media (min-width: 576px) {
    #main-title { font-size: 2.5rem; }
    #main-subtitle { font-size: 1.1rem; }
}

/* Bootstrap md breakpoint: 768px */
@media (min-width: 768px) {
    #main-title { font-size: 3.5rem; }
    #main-subtitle { font-size: 1.3rem; }
}

/* Bootstrap lg breakpoint: 992px */
@media (min-width: 992px) {
    #main-title { font-size: 4.5rem; }
    #main-subtitle { font-size: 1.5rem; }
}

</style>

