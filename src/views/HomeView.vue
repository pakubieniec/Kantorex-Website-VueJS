<script setup>
import Navigation from '@/components/Navigation.vue';
import Footer from '@/components/Footer.vue';
import ExchangeRatesCards from '@/components/ExchangeRatesCards.vue';
import Calculator from '@/components/Calculator.vue';
</script>

<template>
    <Navigation />
  <header class="header">
    <svg id="wave" style="transform:rotate(0deg); transition: 0.3s" viewBox="0 0 1440 150" version="1.1" xmlns="http://www.w3.org/2000/svg"><defs><linearGradient id="sw-gradient-0" x1="0" x2="0" y1="1" y2="0"><stop stop-color="rgba(0, 29, 61, 1)" offset="0%"></stop><stop stop-color="rgba(0, 53, 102, 1)" offset="100%"></stop></linearGradient></defs><path style="transform:translate(0, 0px); opacity:1" fill="url(#sw-gradient-0)" d="M0,45L360,45L720,75L1080,45L1440,75L1800,0L2160,30L2520,105L2880,135L3240,15L3600,45L3960,120L4320,120L4680,75L5040,75L5400,0L5760,60L6120,105L6480,45L6840,30L7200,60L7560,135L7920,105L8280,75L8640,15L8640,150L8280,150L7920,150L7560,150L7200,150L6840,150L6480,150L6120,150L5760,150L5400,150L5040,150L4680,150L4320,150L3960,150L3600,150L3240,150L2880,150L2520,150L2160,150L1800,150L1440,150L1080,150L720,150L360,150L0,150Z"></path></svg>
    <div class="hero pt-5">
      <div class="container-xl">
        <div class="row">
          <div class="col-md-6 text-center">
            <div class="image-container mb-5 px-4">
              <img src="../assets/images/trading-8774164_1280.jpg" alt="" class="img-fluid" />
            </div>
          </div>
          <div class="col-md-6">
            <div
              class="text-container p-4 d-flex flex-column justify-content-center h-100 mb-5"
            >
              <h1 class="display-3 fw-bold">Kantorex</h1>
              <p class="lead">
                Jesteśmy wiodącym kantorem internetowym, oferującym bezpieczne i szybkie usługi wymiany walut. Nasza firma powstała w 2008 roku, z misją dostarczania najwyższej jakości usług finansowych naszym klientom.
              </p>
              <p>Naszą misją jest ułatwienie dostępu do korzystnych kursów walutowych dla klientów indywidualnych oraz biznesowych, zapewniając przy tym pełne bezpieczeństwo transakcji i najwyższy standard obsługi.</p>
            </div>
          </div>
        </div>
        <div class="row">
          <Calculator />
        </div>
      </div>
    </div>
    <svg id="wave" class="wave" style="transform:rotate(180deg); transition: 0.3s" viewBox="0 0 1440 150" version="1.1" xmlns="http://www.w3.org/2000/svg"><defs><linearGradient id="sw-gradient-0" x1="0" x2="0" y1="1" y2="0"><stop stop-color="rgba(0, 29, 61, 1)" offset="0%"></stop><stop stop-color="rgba(0, 53, 102, 1)" offset="100%"></stop></linearGradient></defs><path style="transform:translate(0, 0px); opacity:1" fill="url(#sw-gradient-0)" d="M0,45L360,45L720,75L1080,45L1440,75L1800,0L2160,30L2520,105L2880,135L3240,15L3600,45L3960,120L4320,120L4680,75L5040,75L5400,0L5760,60L6120,105L6480,45L6840,30L7200,60L7560,135L7920,105L8280,75L8640,15L8640,150L8280,150L7920,150L7560,150L7200,150L6840,150L6480,150L6120,150L5760,150L5400,150L5040,150L4680,150L4320,150L3960,150L3600,150L3240,150L2880,150L2520,150L2160,150L1800,150L1440,150L1080,150L720,150L360,150L0,150Z"></path></svg>
  </header>
  <ExchangeRatesCards />
  <Footer />
</template>

<style scoped>
.header {
  margin-top: 40px;
  font-size: 1.2rem;
}

#wave {
  margin-bottom: -2px;
}

#wave.wave {
  margin-top: -10px;
}

.header .hero h1 {
  color: #fffdf7;
}

.header .hero {
  color: #fffdf7;
  background-color: #001d3d;
  width: 100vw;
}

img {
  width: 70%;
  border-radius: 8px;
}

.text-container {
  margin-top: -60px;
}

.btn {
  background-color: #ffd60a;
  color: #001d3d;
  border: 1px solid transparent;
  transition: 0.3s;
}

.btn:hover {
  background-color: #001d3d;
  border: 1px solid #ffd60a;
  color: #ffd60a;
}

@media  (max-width: 768px) {
  header {
    text-align: center;
  }
  img {
    display:block;
    width: 40%;
    margin: 0 auto;
  }

  @media  (max-width: 560px) { 
    img {
      width: 40%;
    }
  
  }
}

</style>


