<template>
<section class="d-flex justify-content-center">
    <form class="p-4 mb-5"  v-for="i in array" :key="i.id">
    <h2>Kalkulator</h2>
    <p class="mb-4">Sprawdź kurs i zobacz ile zyskasz</p>
        <div>
          <div class="input-group">
          <input v-model="amount" type="number" class="form-control" id="inputAmount" placeholder="Posiadam...">
          <select v-model="currency" class="form-select" aria-label="Wybierz walute...">
            <option value="7"> {{i.rates[7].code}}</option>
            <option value="1"> {{i.rates[1].code}}</option>
            <option value="10"> {{i.rates[10].code}}</option>
            <option value="9">{{i.rates[9].code}}</option>
            <option value="13">{{i.rates[13].code}}</option>
          </select>
        </div>
        </div>
        <div class="m-2">
          <div v-show="result">
            <div class="d-flex justify-content-center">
          <p class="calc p-1 mt-2 text-center" @load="currency(option.value)" v-bind="result">Kwota: {{result = amount * i.rates[option].mid}}<span> PLN</span></p>
        </div> </div>
      </div>
      </form>
    </section>
</template>

<script>
export default {
data() {
  return {
      array: [],
      amount: null,
      currency: null,  
      option: 7,
      result: null
    }
},
mounted() {
  fetch('http://api.nbp.pl/api/exchangerates/tables/a/')
  .then(res => res.json())
  .then(data => this.array = data)
  .catch(err => console.log(err.message))
},
watch: {
currency(option){
    this.option = option
    return this.option;
  }
}
}
</script>


<style scoped>
form {
  width: 50%;
  background-color: #fff;
  color: black;
  border-radius: 20px;
}

.input-group {
  border: 2px solid #ffd60a;
  border-radius: 9px;
}

h2,p {
  letter-spacing: 1px;
  color: #001d3d;;
}

h2 {
  font-size:2.4rem;
  margin-bottom: -2px;
}

.calc {
  width: 50%;
  font-size: 1.2rem;
border-bottom: 2px solid #ffd60a;
}

@media (max-width: 890px) {
  form {
    width: 60%;
  }
}

@media (max-width: 690px) {
  form {
    width: 80%;
  }
}
</style>