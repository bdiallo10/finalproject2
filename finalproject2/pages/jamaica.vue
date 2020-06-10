<template>
  <div class="container">
    <TheNavigation />

    <div class="allAboutJamaica">
      <h1>All About Jamaica</h1>
      <p v-for="aboutJamaica in experiences">{{aboutJamaica.about}}</p>
    </div>

    <div class="aboutJamaica">
      <h3>Beaches in Jamaica</h3>
      <img src="@/assets/jamaica.jpg" alt="A picture of a beach in jamaica">
      <img src="@/assets/tower-isle.jpg" alt="A picture of an Island in jamaica">
      <p v-for="aboutJamaica in experiences">{{aboutJamaica.description}}</p>
    </div>

    <div class="topPlacestovisit">
      <h3>Top Restaurant in Jamaica</h3>
      <ul>
        <li v-for="bestRestaurent in topRestaurant">{{bestRestaurent}}</li>
      </ul>
      <h3>Best Beaches in Jamaica</h3>
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
      topRestaurant: ['5050 Lounge Montego Bay', 'Zimbali Mountain Cooking Studio', 'The Lodge Restaurant at Tensing Pen Hotel', 'Kool Vybes Bar and Jerk Centre'],
      beaches: ['Cornwall Beach', 'Silver Sands', 'Mammee Bay Beach', 'Boston Bay Beach', 'Frenchmans Cove', 'Winnifred Beach', 'Calabash Bay Beach', 'Seven Mile Beach', 'Doctor Cave Beach'],
      experiences: [
          {name: "Hawaii Beach"},
          {image: "@/assets/hawaii.jpg"},
          {description:
            "All about Jamaica. Etiam iaculis, ex in semper fringilla, lorem augue maximus lorem, in aliquet ex massa non enim. Maecenas pharetra orci eu semper pharetra. Suspendisse vel elit semper, fringilla metus ac, pulvinar justo. Vestibulum nibh lacus, pellentesque non arcu vel, efficitur eleifend lorem. Duis ultrices bibendum orci, nec laoreet elit. In vulputate massa vel massa cursus gravida. Aliquam sed lacus pulvinar, imperdiet risus at, lacinia dolor. Maecenas pellentesque arcu mattis iaculis efficitur. Maecenas quis sem pulvinar, sodales neque eget, efficitur odio."},
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
