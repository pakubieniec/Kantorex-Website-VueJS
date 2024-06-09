<template>
<Navigation />
    <h2 class="display-4">Kursy złota z ostatnich 30 dni</h2>
    <section class="gold d-flex flex-column align-items-center mb-5" v-if="array.length">
        <div class="gold-details d-flex flex-wrap justify-content-evenly mt-4">
        <div class="badge shadow p-3 w-20 mb-4" v-for="i in array" :key="i.id">
            <svg id='Gold_Bars_24' width='30' height='30' viewBox='0 0 24 24' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink'><rect width='24' height='24' stroke='none' fill='#000000' opacity='0'/>
                <g transform="matrix(0.42 0 0 0.42 12 12)" >
                <g style="" >
                <g transform="matrix(1 0 0 1 0 -1.5)" >
                <path style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(250,177,59); fill-rule: nonzero; opacity: 1;" transform=" translate(-24, -22.5)" d="M 16 36 L 0 36 L 0.333 35 L 12.279 27 C 12.709 27 13.092 27.275 13.228 27.684 L 16 36 z M 32 36 L 16 36 L 16.333 35 L 28.278999999999996 27 C 28.708999999999996 27 29.091999999999995 27.275 29.227999999999998 27.684 L 32 36 z M 48 36 L 32 36 L 32.333 35 L 44.278999999999996 27 C 44.708999999999996 27 45.092 27.275 45.227999999999994 27.684 L 48 36 z M 40 27 L 24 27 L 24.333 26 L 36.278999999999996 18 C 36.708999999999996 18 37.092 18.275 37.227999999999994 18.684 L 40 27 z M 32 18 L 16 18 L 16.333 17 L 28.278999999999996 9 C 28.708999999999996 9 29.091999999999995 9.275 29.227999999999998 9.684 L 32 18 z M 24 27 L 8 27 L 8.333 26 L 20.279 18 C 20.709 18 21.092 18.275 21.228 18.684 L 24 27 z" stroke-linecap="round" />
                </g>
                <g transform="matrix(1 0 0 1 -1.41 -1.5)" >
                <path style="stroke: none; stroke-width: 1; stroke-dasharray: none; stroke-linecap: butt; stroke-dashoffset: 0; stroke-linejoin: miter; stroke-miterlimit: 4; fill: rgb(255,213,79); fill-rule: nonzero; opacity: 1;" transform=" translate(-22.59, -22.5)" d="M 13.17 27.54 L 0 36 L 2.77 27.68 C 2.91 27.28 3.29 27 3.72 27 L 12.280000000000001 27 C 12.66 27 12.99 27.21 13.17 27.54 z M 29.17 27.54 L 16 36 L 18.77 27.68 C 18.91 27.28 19.29 27 19.72 27 L 28.28 27 C 28.66 27 28.99 27.21 29.17 27.54 z M 45.17 27.54 L 32 36 L 34.77 27.68 C 34.910000000000004 27.28 35.290000000000006 27 35.720000000000006 27 L 44.28000000000001 27 C 44.66 27 44.99 27.21 45.17 27.54 z M 37.17 18.54 L 24 27 L 26.77 18.68 C 26.91 18.28 27.29 18 27.72 18 L 36.28 18 C 36.66 18 36.99 18.21 37.17 18.54 z M 29.17 9.54 L 16 18 L 18.77 9.68 C 18.91 9.28 19.29 9 19.72 9 L 28.28 9 C 28.66 9 28.99 9.21 29.17 9.54 z M 21.17 18.54 L 8 27 L 10.77 18.68 C 10.91 18.28 11.29 18 11.719999999999999 18 L 20.28 18 C 20.66 18 20.99 18.21 21.17 18.54 z" stroke-linecap="round" />
                </g>
                </g>
                </g>
                </svg>
                <div>
                    <p>Data: <span class="fw-light">{{i.data}}</span></p>
                    <p>Cena: <span class="fw-light">{{i.cena}}</span></p>
                </div>
            </div>
        </div>
    </section> 
<Footer />
</template>


<script>
import Navigation from '@/components/Navigation.vue';
import Footer from '@/components/Footer.vue';
export default {
    components: {
        Navigation, Footer
    },
    data() {
  return {
      array: [],
  }
},
mounted() {
  fetch('http://api.nbp.pl/api/cenyzlota/last/30/?format=json')
  .then(res => res.json())
  .then(data => this.array = data)
  .catch(err => console.log(err.message))
}
}
</script>

<style scoped>
.gold {
    margin-top: 30px;
    color: #001d3d;
}

.badge {
    width: 21%;
}

p, h1 {
    color: #003566;
}

h2 {
    margin-top: 8rem;
    color: #001d3d;
    text-align: center;
}

.green {
    color: green;
}

@media  (max-width: 1024px) {
    .badge {
        width: 30%;
    }
}

@media  (max-width: 768px) {
    .badge {
        width: 40%;
    }
}

@media  (max-width: 590px) {
    .badge {
        width: 60%;
    }
}
</style>