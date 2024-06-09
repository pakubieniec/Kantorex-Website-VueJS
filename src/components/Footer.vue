<template>
    <footer class="footer mt-5 py-4 shadow d-flex align-items-center">
        <div class="container">
          <div class="row">
            <div class="col-md-8">
              <ul class="nav">
                <li class="nav-item">
                  <RouterLink to="/" href="index.html" class="nav-link">Strona główna</RouterLink>
                </li>
                <li class="nav-item">
                  <RouterLink to="/about" href="#details" class="nav-link">O nas</RouterLink>
                </li>
                <li class="nav-item">
                  <RouterLink to="/contact" href="contact.html" class="nav-link">Kontakt</RouterLink>
                </li>
              </ul>
            </div>
            <div class="col-md-4">
              <p class="text-end d-none d-md-block">
                Copyright &copy; Kantorex 2024
              </p>
            </div>
          </div>
        </div>
      </footer>
</template>

<style scoped>
.footer {
  width: 100vw;
  height: 80px;
  background-color: #fffdf7;
}
.footer .nav-link,
.footer p {
  color: #001d3d;
}

.footer .nav-link {
  color: #001d3d;
  border-bottom: 3px solid transparent;
  transition: 0.5s;
}
.footer .nav-link:hover {
  color: #003566;
  transform: scale(1.1);
  border-bottom: 3px solid #ffd60a;
}
</style>