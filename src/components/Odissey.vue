<script setup>
import { onMounted, ref } from 'vue';
import Footer from './Footer.vue';
import Header from './Header.vue';

const titleRef = ref(null);
const introSlogan = ref("DEFY THE GODS, TRAIN THE MACHINE")
onMounted(() => {
  titleRef.value.textContent = titleRef.value.textContent.toUpperCase();
});

function scrollToSection() {
  document.getElementById('section-two').scrollIntoView({ behavior: 'smooth' });
}
</script>

<template>
    <div class="d-flex flex-column">
        <Header></Header>
        <!-- Hero Section -->
        <div class="d-flex flex-column justify-content-center align-items-center min-vh-100 text-center">
            <div class="container px-4 px-md-5 mt-5">
                <h1 id="main-title" class="display-4 text-center mx-auto" ref="titleRef">The Odissey of Machine Learning</h1>
                <p id="main-text" class="mb-5 mx-auto text-center" v-html="introSlogan"></p>
            </div>
            <div class="scroll-arrow" @click="scrollToSection">&#8595;</div>
        </div>

        <!-- Section Two -->
        <section id="section-two" class="min-vh-100 d-flex align-items-center">
            <div class="container px-4 px-md-5 py-5 w-100">
                <div class="row g-5 align-items-center">
                    <div class="col-12 col-md-6">
                        <h2 class="section-title">THE JOURNEY BEGINS</h2>
                        <p class="section-text">
                            Machine learning is not merely a tool — it is an odyssey. A quest through data, patterns, and the unknown, forging intelligence from the raw material of experience.
                        </p>
                        <p class="section-text">
                            Every model trained is a step further into uncharted territory. Every iteration, a battle won against chaos. The machine learns. And so do we.
                        </p>
                        <div class="section-divider"></div>
                    </div>
                    <div class="col-12 col-md-6">
                    </div>
                </div>
            </div>
        </section>

        <Footer></Footer>
    </div>
</template>

<style scoped>

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(10px); }
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
    font-size: 1.8rem;
    animation: fadeSlideUp 0.9s cubic-bezier(0.22, 1, 0.36, 1) forwards;
}

#main-subtitle {
    color: var(--red-color);
    font-family: OdisseyFont, sans-serif;
    font-size: 0.75rem;
    opacity: 0;
    animation: fadeSlideUp 0.9s cubic-bezier(0.22, 1, 0.36, 1) 0.45s forwards;
}

#main-text {
    color: var(--red-color);
    letter-spacing: 4px;
    max-width: 900px;
    margin: 0.5rem auto 0;
    font-family: OdisseyFont, sans-serif;
    opacity: 0;
    animation: fadeSlideUp 0.9s cubic-bezier(0.22, 1, 0.36, 1) 0.9s forwards;
}

.scroll-arrow {
    color: var(--red-color);
    font-size: 2rem;
    margin-bottom: 2rem;
    animation: bounce 1.4s ease-in-out infinite;
    opacity: 0.7;
    cursor: pointer;
    transition: opacity 0.2s;
}

.scroll-arrow:hover {
    opacity: 1;
}

/* Section Two */
#section-two {
    background-color: var(--dark-color);
    border-top: 1px solid rgba(47, 94, 141, 0.2);
}

.section-title {
    font-family: OdisseyFont, sans-serif;
    color: var(--blue-color);
    font-size: 1.8rem;
    letter-spacing: 4px;
    margin-bottom: 1.5rem;
}

.section-text {
    color: rgba(255, 255, 255, 0.7);
    font-family: OdisseyFont, sans-serif;
    font-size: 0.85rem;
    letter-spacing: 2px;
    line-height: 1.9;
    margin-bottom: 1rem;
}

.section-divider {
    width: 60px;
    height: 3px;
    background-color: var(--red-color);
    margin-top: 2rem;
}

@media (min-width: 768px) {
    .section-title { font-size: 2.4rem; }
    .section-text { font-size: 0.95rem; }
}

/* Bootstrap sm breakpoint: 576px */
@media (min-width: 576px) {
    #main-title { font-size: 2.5rem; }
    #main-subtitle { font-size: 1.1rem; }
    #main-text { font-size: 1.1rem; }
}

/* Bootstrap md breakpoint: 768px */
@media (min-width: 768px) {
    #main-title { font-size: 3.5rem; }
    #main-subtitle { font-size: 1.3rem; }
    #main-text { font-size: 1.2rem; }
}

/* Bootstrap lg breakpoint: 992px */
@media (min-width: 992px) {
    #main-title { font-size: 4.5rem; }
    #main-subtitle { font-size: 1.5rem; }
    #main-text { font-size: 1.35rem; }
}

</style>

