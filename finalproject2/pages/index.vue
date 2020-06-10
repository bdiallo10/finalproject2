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


    <footer>
      <TheNavigation />
    </footer>
  </div>

</template>

<script>

import TheNavigation from "@/components/TheNavigation";


export default {
  components: {
    TheNavigation
  },
  data() {
    return {
      countries: ['Brazil', 'Hawaii', 'Jamaica', 'Panama']
    }
  }
};

</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}
</style>
