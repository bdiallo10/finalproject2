<template>
  <div class="container">
    <TheNavigation />

    <div class="aboutHawaii">
      <h1>All About Hawaii</h1>
      <p v-for="aboutHawaii in experiences">{{aboutHawaii.about}}</p>
    </div>

    <div class="experienceHawaii">
      <h3 v-for="hawaiiBeach in experiences">{{hawaiiBeach.name}}</h3>
      <img src="@/assets/hawaii.jpg" alt="A picture of a beach in hawaii">
      <img src="@/assets/waikiki-beach.jpg" alt="A picture of waikiki beach">
      <p v-for="aboutHawaiiBeach in experiences">{{aboutHawaiiBeach.description}}</p>
    </div>

    <div class="topPlaces">
      <h3>Top 4 Food Truck</h3>
      <ul>
        <li v-for="bestFoodTruck in foodTruck">{{bestFoodTruck}}</li>
      </ul>
      <h3>Best Beaches</h3>
      <ul>
        <li v-for="bestBeaches in beaches">{{bestBeaches}}</li>
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
      foodTruck: ['Mediterranean Grill', 'Like Poke?', 'Horhitos Mobile Taqueria', 'Thai Mee Up'],
      beaches: ['Lahaina, Maui', 'Kailua, Oahu', 'Haleiwa, Oahu', 'Waikiki, Oahu', 'Kailua-Kona, Big Island', 'Hawi, Big Island', 'Hilo, Big Island', 'Hanalei, Kauai', 'Kapa’a, Kauai'],
      experiences: [
          {name: "Hawaii Beach"},
          {image: "@/assets/hawaii.jpg"},
          {description:
            "All about hawaii. Etiam iaculis, ex in semper fringilla, lorem augue maximus lorem, in aliquet ex massa non enim. Maecenas pharetra orci eu semper pharetra. Suspendisse vel elit semper, fringilla metus ac, pulvinar justo. Vestibulum nibh lacus, pellentesque non arcu vel, efficitur eleifend lorem. Duis ultrices bibendum orci, nec laoreet elit. In vulputate massa vel massa cursus gravida. Aliquam sed lacus pulvinar, imperdiet risus at, lacinia dolor. Maecenas pellentesque arcu mattis iaculis efficitur. Maecenas quis sem pulvinar, sodales neque eget, efficitur odio."},
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
