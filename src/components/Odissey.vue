<script setup>
import { onMounted, ref } from 'vue';
import Footer from './Footer.vue';
import Header from './Header.vue';

const titleRef = ref(null);
const introText = ref(`The Odyssey of Machine Learning is a side project built on my own from scratch with the Vue JavaScript framework. The goal is to teach people what machine learning is and how it works, through the analogy of Ulysses' journey to get home.<br>
I, of course, got the inspiration from the upcoming release of Christopher Nolan's adaptation, which is about to open on July 14th, 2026, in American theatres.<br>
At the end of the module, you will know the fundamental stages of the machine learning process! Don't hesitate to submit ideas for improving the module, or if you have any questions!`);

onMounted(() => {
  titleRef.value.textContent = titleRef.value.textContent.toUpperCase();
});
</script>

<template>
    <div class="d-flex flex-column min-vh-100">
        <Header></Header>
        <div class="d-flex flex-column justify-content-center align-items-center flex-grow-1 text-center">
            <div class="container px-4 px-md-5 pt-5 mt-5">
                <h1 id="main-title" class="display-4 fw-bold text-center mx-auto" ref="titleRef">The Odissey of Machine Learning</h1>
                <p id="main-text" class="mb-5 mx-auto text-center lh-lg" v-html="introText"></p>
            </div>
            <div class="scroll-arrow">&#8595;</div>
        </div>
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
    font-size: 0.rem;
    text-transform: uppercase;
    line-height: 2;
    letter-spacing: 4px;
    width: 100%;
    max-width: 900px;
    margin: 3rem auto 0;
    white-space: pre-line;
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

