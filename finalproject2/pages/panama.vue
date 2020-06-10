<template>
  <div class="container">
    <TheNavigation />

    <div class="allaboutPanama">
      <h1>All About Panama</h1>
      <p v-for="aboutPanama in experiences">{{aboutPanama.description}}</p>
    </div>

    <div class="">
      <img src="@/assets/panama.jpg" alt="A picture of a beach in panama">
      <img src="@/assets/panama-city.jpg" alt="A picture of panama city">
      <img src="@/assets/panama-canal.jpg" alt="A picture of boats in Panama">
      <img src="@/assets/tower-isle.jpg" alt="A picture of an Island in jamaica">
    </div>

    <div class="mustVisit">
      <h3>Places in Panama that is a Must to visit</h3>
      <ul>
        <li v-for="awesomerestaurant in restaurant">{{awesomerestaurant}}</li>
      </ul>
      <ul>
        <li v-for="bestbeaches in beaches">{{bestbeaches}}</li>
      </ul>
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
  data () {
    return {
      restaurant: ['Oak Restauran', 'La Fabrica', 'La Negra Tomasa', 'Donde Jose'],
      beaches: ['Beaches of the San Blas Islands', 'Red Frog Beach', 'Starfish Beach', 'Isla Coiba in Coiba National Park', 'Bluff Beach', 'Punta Chame'],
      experiences: [
          {name: "Hawaii Beach"},
          {image: "@/assets/hawaii.jpg"},
          {description:
            "All about Panama. Etiam iaculis, ex in semper fringilla, lorem augue maximus lorem, in aliquet ex massa non enim. Maecenas pharetra orci eu semper pharetra. Suspendisse vel elit semper, fringilla metus ac, pulvinar justo. Vestibulum nibh lacus, pellentesque non arcu vel, efficitur eleifend lorem. Duis ultrices bibendum orci, nec laoreet elit. In vulputate massa vel massa cursus gravida. Aliquam sed lacus pulvinar, imperdiet risus at, lacinia dolor. Maecenas pellentesque arcu mattis iaculis efficitur. Maecenas quis sem pulvinar, sodales neque eget, efficitur odio."},
          {about:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
          },
      ],
    }
  },
};
</script>

<style>

</style>
