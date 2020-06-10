<template>
  <div class="container">
    <div class="navbar">
        <TheNavigation />
    </div>

    <div class="gallery">
      <img src="@/assets/iguacu-falls.jpg" alt="A waterfall picture">
      <img src="@/assets/hawaii.jpg" alt="A picture of a beach in hawaii">
      <img src="@/assets/brazil.jpg" alt="A picture from Brazil">
      <img src="@/assets/jamaica.jpg" alt="A picture from Jamaica">
      <img src="@/assets/panama-city.jpg" alt="A picture of panama city">
      <img src="@/assets/waikiki-beach.jpg" alt="A picture of waikiki beach">

    </div>

    <!-- <div class="wrapper">
        <h1 class="heading">Countries of Europe</h1>
        <section class="container" v-if="countries">
            <card
              v-for="country of countries"
              :key="country.id"
              :country="country"
            />
        </section>
    </div> -->


    <footer>
      <TheNavigation />
    </footer>
  </div>

</template>

<script>

import TheNavigation from "@/components/TheNavigation";
// import Card from '~/components/Card.vue'
// import axios from 'axios'


export default {
  components: {
    TheNavigation
    // Card
  },
  data() {
    return {
      countries: ['Brazil', 'Hawaii', 'Jamaica', 'Panama']
    }
  }
  // data() {
  //   return {
  //     loading: true,
  //     countries: null,
  //     errored: false
  //   }
  // },
  // mounted () {
  // axios
  //   .get('https://restcountries.eu/rest/v2/region/americas')
  //   .then(response => (this.countries = response.data))
  //   .catch(error => {
  //     console.log(error)
  //     this.errored = true
  //   })
  //   .finally(() => this.loading = false)
  // }
};

</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}
</style>
