<template>
    <h2 class="display-4">Kursy walut</h2>
    <div class="cards d-flex flex-wrap justify-content-evenly">
<div class="card border-0 shadow p-3" if="array.length">
  <div class="card-body">
      <div v-for="item in array" :key="item.id">
          <div class="d-flex align-items-center">
              <img src="../assets/images/eur.webp" alt="">
          <h5 class="card-title ms-3">Kurs Euro
          </h5>
      </div>
          <div class="d-flex justify-content-evenly align-items-start mt-5">
              <h5 class="card-text card-text-lg">
                  {{item.rates[7].code}}
              </h5>
              <div class="d-flex flex-column align-items-center justify-content-center">
                  <p class="card-text card-text-md fw-light">{{(item.rates[7].mid + 0.20).toFixed(4)}}</p>
                  <p class="lead card-text-sm"><span class="badge p-2">Kupno</span></p>
              </div>
             <div class="d-flex flex-column align-items-center justify-content-center">
              <p class="card-text card-text-md fw-light">{{(item.rates[7].mid - 0.20).toFixed(4)}}</p>
               <p class="lead card-text-sm"><span class="badge p-2">Sprzedaz</span></p>
          </div>
          </div>
  </div>
      </div>
    </div>
    <div class="card border-0 shadow p-3" if="array.length">
      <div class="card-body">
          <div v-for="item in array" :key="item.id">
              <div class="d-flex align-items-center">
                  <img src="../assets/images/usa.webp" alt="">
              <h5 class="card-title ms-3">Kurs Dolara amerykańskiego
              </h5>
       </div>
              <div class="d-flex justify-content-evenly align-items-start mt-5">
                  <h5 class="card-text card-text-lg">
                      {{item.rates[1].code}}
                  </h5>
                  <div class="d-flex flex-column align-items-center justify-content-center">
                      <p class="card-text card-text-md fw-light">{{(item.rates[1].mid + 0.20).toFixed(4)}}</p>
                      <p class="lead card-text-sm"><span class="badge p-2">Kupno</span></p>
                  </div>
                 <div class="d-flex flex-column align-items-center justify-content-center">
                  <p class="card-text card-text-md fw-light">{{(item.rates[1].mid - 0.20).toFixed(4)}}</p>
                   <p class="lead card-text-sm"><span class="badge p-2">Sprzedaz</span></p>
              </div>
              </div>
      </div>
          </div>
        </div>
        <div class="card border-0 shadow p-3" if="array.length">
          <div class="card-body">
              <div v-for="item in array" :key="item.id">
                  <div class="d-flex align-items-center justify-content-center">
                      <img src="../assets/images/uk.webp" alt="">
                  <h5 class="card-title ms-3">Kurs Funta Brytyjskiego
                  </h5>
              </div>
                  <div class="d-flex justify-content-evenly align-items-start mt-5">
                      <h5 class="card-text card-text-lg">
                          {{item.rates[10].code}}
                      </h5>
                      <div class="d-flex flex-column align-items-center justify-content-center">
                          <p class="card-text card-text-md fw-light">{{(item.rates[10].mid + 0.20).toFixed(4)}}</p>
                          <p class="lead card-text-sm"><span class="badge p-2">Kupno</span></p>
                      </div>
                     <div class="d-flex flex-column align-items-center justify-content-center">
                      <p class="card-text card-text-md fw-light">{{(item.rates[10].mid - 0.20).toFixed(4)}}</p>
                       <p class="lead card-text-sm"><span class="badge p-2">Sprzedaz</span></p>
                  </div>
                  </div>
           </div>
              </div>
            </div>
            <div class="card border-0 shadow p-3" if="array.length">
              <div class="card-body">
                  <div v-for="item in array" :key="item.id">
                      <div class="d-flex align-items-center">
                          <img src="../assets/images/switz.webp" alt="">
                      <h5 class="card-title ms-3">Kurs Franka Szajcarskiego
                      </h5>
                   </div>
                      <div class="d-flex justify-content-evenly align-items-start mt-5">
                          <h5 class="card-text card-text-lg">
                              {{item.rates[9].code}}
                          </h5>
                          <div class="d-flex flex-column align-items-center justify-content-center">
                              <p class="card-text card-text-md fw-light">{{(item.rates[9].mid + 0.20).toFixed(4)}}</p>
                              <p class="lead card-text-sm"><span class="badge p-2">Kupno</span></p>
                          </div>
                         <div class="d-flex flex-column align-items-center justify-content-center">
                          <p class="card-text card-text-md fw-light">{{(item.rates[9].mid - 0.20).toFixed(4)}}</p>
                           <p class="lead card-text-sm"><span class="badge p-2">Sprzedaz</span></p>
                      </div>
                      </div>
             </div>
                  </div>
                </div>
                <div class="card border-0 shadow p-3" if="array.length">
                  <div class="card-body">
                      <div v-for="item in array" :key="item.id">
                          <div class="d-flex align-items-center">
                              <img src="../assets/images/cze.png" alt="">
                          <h5 class="card-title ms-3">Kurs Korony Czeskiej
                          </h5>
                      </div>
                          <div class="d-flex justify-content-evenly align-items-start mt-5">
                              <h5 class="card-text card-text-lg">
                                  {{item.rates[13].code}}
                              </h5>
                              <div class="d-flex flex-column align-items-center justify-content-center">
                                  <p class="card-text card-text-md fw-light">{{(item.rates[13].mid + 0.020).toFixed(4)}}</p>
                                  <p class="lead card-text-sm"><span class="badge p-2">Kupno</span></p>
                              </div>
                             <div class="d-flex flex-column align-items-center justify-content-center">
                              <p class="card-text card-text-md fw-light">{{(item.rates[13].mid - 0.020).toFixed(4)}}</p>
                               <p class="lead card-text-sm"><span class="badge p-2">Sprzedaz</span></p>
                          </div>
                          </div>
                  </div>
                      </div>
                    </div>
        <div class="card border-0 shadow p-3 d-flex align-items-center justify-content-center">
      <RouterLink to="/exchangeRates" href="index.html" class="btn">Zobacz więcej</RouterLink>
    </div>
  </div>
  

</template>
<script>
import useSWR, { preload } from 'svr';
export default {
data() {
  return {
      array: [],
  }
},
mounted() {
    const fetcher = fetch('http://api.nbp.pl/api/exchangerates/tables/a/')
  .then(res => res.json())
  .then(data => this.array = data)
  .catch(err => console.log(err.message))

  preload('/api/user', fetcher)
  Profile()
//   profie() {
//     const {data, error} = useSWR('/api/user', fetcher)
//   }
},
}
</script>

<style scoped>
.cards {
    margin-top: 3rem;
}

.card {
width: 32%;
background-color: #fffdf7;
color: #001d3d;
margin-bottom: 2rem;
}

.card-title {
font-size: 1rem;
text-transform: uppercase;
}

.card-text-lg {
font-size: 1.8rem;
}

.card-text-md {
font-size: 1.6rem;
}

.card-text-sm{
margin-top: -10px;
font-size: 1rem;
}

.badge {
background-color: #ffd60a;
color:#001d3d;
}

.btn {
width: 60%;
background-color: #003566;
color:#fffdf7;
border-radius: 10px;
cursor: pointer;
padding: 10px 0;
letter-spacing: 1.5px;
border: 1px solid transparent;
transition: 0.3s;
}

.btn:hover {
background-color: #fffdf7;
color:#003566;
border: 1px solid #003566;
transform: scale(1.1);
}

img{
  width: 20%;
  border-radius: 5px ;
}

h2 {
    margin-top: 3rem;
    color: #001d3d;
    text-align: center;
}

@media  (max-width: 1024px) {
.cardd {
  flex-wrap: wrap;
  align-items: center;
}
   .card {
      width: 44%;
      margin-bottom: 20px;
  }
}

@media  (max-width: 760px) {
   .card {
      width: 80%;
      margin-bottom: 20px;
  }
}
</style>