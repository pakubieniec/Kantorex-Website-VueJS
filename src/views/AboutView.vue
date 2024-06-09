<script setup>
import Navigation from '../components/Navigation.vue'
import Footer from '@/components/Footer.vue';
</script>

<template>
  <div class="about">
    <Navigation />
    <section class="about text-center">
      <h2 class="display-4">O Nas</h2>
      <div class="about-details d-flex justify-content-between align-items-center mt-5">
        <div class="box-about"><img src="../assets/images/kimJestesmyPhoto.jpg" alt=""></div>
        <div class="box-about">
          <h3>Kim jesteśmy?</h3>
          <p>Jesteśmy wiodącym kantorem internetowym, oferującym bezpieczne i szybkie usługi wymiany walut online. Nasza firma powstała w [rok założenia], z misją dostarczania najwyższej jakości usług finansowych naszym klientom.</p></div>
      </div>
      <div class="about-details d-flex justify-content-between align-items-center mt-5">
        <div class="box-about order-md-1">
          <h3>Nasze wartości</h3>
          <p>Naszą misją jest ułatwienie dostępu do korzystnych kursów walutowych dla klientów indywidualnych oraz biznesowych, zapewniając przy tym pełne bezpieczeństwo transakcji i najwyższy standard obsługi.</p></div>
          <div class="box-about order-md-5"><img src="../assets/images/naszaWartosciPhoto.jpg" alt=""></div>
      </div>
      <div class="about-details d-flex justify-content-between align-items-center mt-5">
        <div class="box-about"><img src="../assets/images/naszaMisjaPhoto.jpg" alt=""></div>
        <div class="box-about">
          <h3>Nasza misja</h3>
          <p>Naszym celem na przyszłość jest dalszy rozwój i ekspansja na rynki międzynarodowe. Planujemy wprowadzenie nowych usług finansowych oraz rozwijanie naszej oferty, aby sprostać oczekiwaniom nawet najbardziej wymagających klientów.</p>
      </div>
      </div>
      <div class="about-details d-flex justify-content-between align-items-center mt-5">
        <div class="box-about">
          <h3>Główne wytyczne</h3>
          <p>Zaufanie: Dbamy o transparentność i uczciwość w relacjach z klientami.</p>
          <p>Innowacyjność: Stale rozwijamy nasze technologie, aby zapewnić najlepsze doświadczenia użytkownikom.</p>
          <p>
            Bezpieczeństwo: Gwarantujemy najwyższe standardy ochrony danych i środków finansowych.</p>
          <p>Profesjonalizm: Nasi specjaliści są zawsze gotowi do pomocy i wsparcia na każdym etapie korzystania z naszych usług.</p></div>
          <div class="box-about"><img src="../assets/images/glowneWytycznePhoto.jpg" alt=""></div>
      </div>
    </section>
  </div>
  <Footer />
</template>

<style scoped>
.about {
  width: 90%;
  margin: 50px auto ;
  color: #001d3d;
}

.box-about {
  width: 50%;
}

h2 {
    margin-top: 5rem;
    color: #001d3d;
    text-align: center;
}

h3 {
  display:inline-block;
  text-align: center;
  margin-bottom: 1rem;
  padding: 0.5rem;
  border-bottom: 2px solid #ffd60a;
}

img {
  width: 80%;
  border-radius: 8px;
  margin: 2rem 0;
  -webkit-box-shadow: 8px 8px 24px 0px rgba(66, 68, 90, 1);
-moz-box-shadow: 8px 8px 24px 0px rgba(66, 68, 90, 1);
box-shadow: 8px 8px 24px 0px rgba(66, 68, 90, 1);
}

@media (max-width: 640px) {
  .box-about {
    width: 100%;
  }
  .about-details {
    flex-direction: column;
  }
}
</style>
