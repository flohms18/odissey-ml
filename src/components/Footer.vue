<template>
  <footer class="odissey-footer d-flex flex-column justify-content-center align-items-center text-center px-3">
    <h2 class="footer-title mb-1">THE ODISSEY OF MACHINE LEARNING</h2>
    <p class="footer-signature mb-0">Made by F.T</p>
  </footer>
</template>

<style scoped>
.odissey-footer {
  min-height: 10vh;
  color: var(--blue-color);
  font-family: OdisseyFont, sans-serif;
  letter-spacing: 4px;
  border-top: 1px solid var(--red-color);
}

.footer-title {
  font-size: 0.6rem;
}

.footer-signature {
  font-size: 0.55rem;
  opacity: 0.6;
}

@media (min-width: 576px) {
  .footer-title { font-size: 0.7rem; }
  .footer-signature { font-size: 0.6rem; }
}

@media (min-width: 768px) {
  .footer-title { font-size: 0.8rem; }
  .footer-signature { font-size: 0.65rem; }
}

@media (min-width: 992px) {
  .footer-title { font-size: 0.85rem; }
  .footer-signature { font-size: 0.7rem; }
}
</style>
