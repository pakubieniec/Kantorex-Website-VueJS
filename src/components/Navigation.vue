<template>
    <nav class="navbar navbar-expand-lg fixed-top navbar-light">
        <div class="container">
          <RouterLink to="/" href="index.html" class="navbar-brand">
            <img src="../assets/images/logo2.png"  alt="" width="225" />
          </RouterLink>
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarNavDropdown"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNavDropdown">
            <ul class="navbar-nav ms-auto">
              <li class="nav-item mx-2">
                <RouterLink to="/" class="nav-link fw-semibold ">Strona główna</RouterLink>
              </li>
              <li class="nav-item mx-2">
                <RouterLink to="/about" class="nav-link fw-semibold">O nas</RouterLink>
              </li>
              <li class="nav-item mx-2">
                <RouterLink to="/exchangeRates" class="nav-link fw-semibold">Kursy walut</RouterLink>
              </li>
              <li class="nav-item mx-2">
                <RouterLink to="/exchangeGold" class="nav-link fw-semibold">Kursy złota</RouterLink>
              </li>
              <li class="nav-item mx-2">
                <RouterLink to="/contact"
                  class="nav-link fw-semibold"
                  >Kontakt</RouterLink
                >
              </li>
            </ul>
          </div>
        </div>
      </nav>
</template>

<style scoped>
.navbar {
  height: 80px;
  background-color: #fffdf7;
}

.navbar img {
  display: block;
  width: 55%;
  height:55%;
}

.navbar .nav-link {
  color: #001d3d;
  border-bottom: 3px solid transparent;
  transition: 0.5s;
}

.navbar .nav-link:hover {
  color: #003566;
  transform: scale(1.1);
  border-bottom: 3px solid #ffd60a;
}

.navbar-nav {
  background-color: #fffdf7;
  justify-content: center;
  align-items: center;
  padding-bottom: 1.6rem;
}
</style>