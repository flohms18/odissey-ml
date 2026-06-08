<template>
    <header>
  <nav class="navbar navbar-expand-lg navbar-dark nav-themed">
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ml-auto">
        <li class="nav-item">
          <a class="nav-btn mx-1" href="#">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-btn mx-1" href="#">Bonus</a>
        </li>
      </ul>
    </div>
  </nav>
  </header>
</template>

<style scoped>
.nav-themed {
  background-color: var(--dark-color);
  letter-spacing: 4px;
}

.nav-btn {
  font-family: OdisseyFont, sans-serif;
  text-transform: uppercase;
  color: var(--blue-color);
  padding: 6px 16px;
  text-decoration: none;
  display: inline-block;
  transition: border-color 0.2s, color 0.2s;
}

.nav-btn:hover {
  border-color: var(--red-color);
  color: var(--red-color);
  text-decoration: none;
}
</style>
