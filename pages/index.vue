<template>
  <NuxtLayout :name="layout">
    <div
      class="custom-container mx-auto mb-10 max-w-screen-2xl px-6 py-10 sm:px-8"
    >
      <h1 class="mb-6 mt-6 text-3xl font-semibold">Explorer Airbnb</h1>
      <div class="flex flex-row gap-3">
        <CardHorizontal
          v-for="card in CardHorizontal"
          :name="card.name"
          :img="card.img"
        />
      </div>

      <h1 class="mb-2 mt-12 text-3xl font-semibold">
        Découvrez les aventures Airbnb
      </h1>

      <h1 class="mb-4 text-xl font-normal md:w-1/2">
        Voyages de plusieurs jours organisés par des experts locaux avec
        activités, repas et logements compris
      </h1>
      <!-- card 6 -->
      <div
        class="pt-12"
        v-if="pending"
      >
        <div class="mb-6 grid grid-cols-2 gap-4 sm:grid-cols-3 lg:grid-cols-6">
          <CardSkeleton
            v-for="index in 6"
            :key="index"
          />
        </div>
      </div>
      <div v-else>
        <div class="grid grid-cols-2 gap-4 sm:grid-cols-3 lg:grid-cols-6">
          <Card
            v-for="card in cardImage1Per6"
            :name="card.name"
            :img="card.img"
          />
        </div>
      </div>

      <h1 class="mb-2 mt-12 text-3xl font-semibold">
        Hébergements Airbnb Plus
      </h1>
      <h1 class="mb-4 text-xl font-normal">
        Une sélection de logements vérifiés selon des critères de qualité et de
        design
      </h1>

      <div class="w-full overflow-hidden rounded-xl shadow-lg">
        <img
          class="w-full transition-all duration-300 ease-out hover:scale-105"
          src="img/Big_Card.png"
          alt=""
        />
      </div>
      <h1 class="mb-6 mt-12 text-3xl font-semibold">
        Logements dans le monde entier
      </h1>
      <!-- Card 4 -->
      <div
        class="pt-12"
        v-if="pending"
      >
        <div class="mb-6 grid grid-cols-2 gap-4 sm:grid-cols-4 lg:grid-cols-4">
          <CardSkeleton
            v-for="index in 8"
            :key="index"
          />
        </div>
      </div>
      <div v-else>
        <div class="grid grid-cols-2 gap-4 sm:grid-cols-3 lg:grid-cols-6">
          <Card
            v-for="card in cardImage1Per6_2"
            :name="card.name"
            :img="card.img"
          />
        </div>
      </div>

      <h1 class="mb-2 mt-12 text-3xl font-semibold">
        Expériences très bien notées
      </h1>

      <h1 class="mb-4 text-xl font-normal md:w-1/2">
        Voyages de plusieurs jours organisés par des experts locaux avec
        activités, repas et logements compris
      </h1>

      <!-- Card 6 -->
      <div
        class="pt-12"
        v-if="pending"
      >
        <div class="mb-6 grid grid-cols-2 gap-4 sm:grid-cols-3 lg:grid-cols-6">
          <CardSkeleton
            v-for="index in 6"
            :key="index"
          />
        </div>
      </div>
      <div v-else>
        <div class="grid grid-cols-2 gap-4 sm:grid-cols-3 lg:grid-cols-6">
          <Card
            v-for="card in cardImage1Per6_2"
            :name="card.name"
            :img="card.img"
          />
        </div>
      </div>

      <h1 class="mb-2 mt-12 text-3xl font-semibold">
        Destinations Airbnb Plus à la Une
      </h1>

      <h1 class="mb-4 text-xl font-normal md:w-1/2">
        Voyages de plusieurs jours organisés par des experts locaux avec
        activités, repas et logements compris
      </h1>
      <!-- card 3 -->
      <div
        class="pt-12"
        v-if="pending"
      >
        <div class="mb-6 grid grid-cols-2 gap-4 sm:grid-cols-3">
          <CardSkeleton
            v-for="index in 3"
            :key="index"
          />
        </div>
      </div>
      <div v-else>
        <div class="grid grid-cols-1 gap-4 sm:grid-cols-3">
          <Card
            v-for="card in cardImage1Per3"
            :name="card.name"
            :img="card.img"
            :description="`À partir de 577€/personne - 3 jours`"
          />
        </div>
      </div>
    </div>
  </NuxtLayout>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      layout: 'custom',
      CardHorizontal: [
        {
          name: 'Logements',
          img: '/card3pcs/1.png',
        },
        {
          name: 'Experience',
          img: '/card3pcs/2.png',
        },
        {
          name: 'Adventures',
          img: '/card3pcs/3.png',
        },
      ],
      cardImage1Per6: [],
      cardImage1Per6_2: [],
      cardImage1Per4: [],
      cardImage1Per3: [],
      pending: true,
    };
  },
  methods: {
    setCardImage1Per6(data) {
      this.cardImage1Per6 = data;
    },
    setCardImage1Per6_2(data) {
      this.cardImage1Per6_2 = data;
    },
    setCardImage1Per4(data) {
      this.cardImage1Per4 = data;
    },
    setCardImage1Per3(data) {
      this.cardImage1Per3 = data;
    },
  },
  mounted() {
    axios
      .get('https://gbyuiq.sse.codesandbox.io/card1per6')
      .then(response => {
        this.setCardImage1Per6(response.data.slice(6, 12));
        this.pending = false; // Update pending state after successful request
      })
      .catch(error => {
        console.log('Gagal :', error);
        this.pending = false; // Update pending state even if there's an error
      });
    axios
      .get('https://gbyuiq.sse.codesandbox.io/card1per6')
      .then(response => {
        this.setCardImage1Per6_2(response.data.slice(0, 6));
        this.pending = false; // Update pending state after successful request
      })
      .catch(error => {
        console.log('Gagal :', error);
        this.pending = false; // Update pending state even if there's an error
      });
    axios
      .get('https://gbyuiq.sse.codesandbox.io/card1per4')
      .then(response => {
        this.setCardImage1Per4(response.data);
        this.pending = false; // Update pending state after successful request
      })
      .catch(error => {
        console.log('Gagal :', error);
        this.pending = false; // Update pending state even if there's an error
      });
    axios
      .get('https://gbyuiq.sse.codesandbox.io/card1per3')
      .then(response => {
        this.setCardImage1Per3(response.data);
        this.pending = false; // Update pending state after successful request
      })
      .catch(error => {
        console.log('Gagal :', error);
        this.pending = false; // Update pending state even if there's an error
      });
  },
};

// const { data: products } = useFetch('https://fakestoreapi.com/products');
// console.log(products);

// const { data: movie } = useFetch(
//   'https://api.themoviedb.org/3/movie/popular?api_key=35d428792ace5959fdc3f64e2ecc08b6'
// );
// console.log(movie);
</script>
