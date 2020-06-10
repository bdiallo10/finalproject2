<template>
  <div class="container">
      <TheNavigation />

      <div class="aboutBrazil">
        <h1>All About Brazil</h1>
        <p v-for="aboutBrazil in experiences">{{aboutBrazil.about}}</p>
      </div>

      <div class="experiencesBrazil">
        <h1 v-for="IguaçuFalls in experiences">{{IguaçuFalls.name}}</h1>
        <img src="@/assets/iguacu-falls.jpg" alt="A waterfall picture">
        <img src="@/assets/brazil.jpg" alt="A picture from Brazil">
        <p v-for="aboutIguaçuFalls in experiences">{{aboutIguaçuFalls.description}}</p>
      </div>

      <div class="citytovisit">
        <h3>Top 12 City in Brazil</h3>
        <ul>
          <li v-for="city in cities">{{city}}</li>
        </ul>
        <h3>Famous Soccer Place</h3>
        <ul>
          <li v-for="famous in soccer">{{famous}}</li>
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
      soccer: ['Pele', 'Neymar', 'Ronaldo Fenomeno', 'Ronaldihno'],
      cities: ['Rio de Janeiro', 'Sao Paulo', 'Brasília', 'Natal', 'Fortaleza', 'Salvador da Bahia', 'Manaus', 'Recife', 'Cuiaba', 'Curitiba', 'Porto Alegre', 'Belo Horizonte'],
      experiences: [
          {name: "Iguaçu Falls"},
          {image: "@/assets/iguacu-falls.jpg"},
          {description:
            "Suspendisse lobortis pharetra tempor. Cras eleifend ante sed arcu interdum, in bibendum enim ultricies. Integer rutrum quis risus at tempor. Maecenas facilisis, nisi vel pellentesque maximus, lectus felis malesuada purus, a pulvinar elit est quis turpis. Duis convallis purus quis finibus consequat. Pellentesque faucibus tincidunt augue non consequat. Donec fringilla at est sit amet blandit. Nunc at porttitor ligula. Fusce sed odio turpis. Suspendisse lobortis pharetra tempor. Cras eleifend ante sed arcu interdum, in bibendum enim ultricies. Integer rutrum quis risus at tempor. Maecenas facilisis, nisi vel pellentesque maximus, lectus felis malesuada purus, a pulvinar elit est quis turpis. Duis convallis purus quis finibus consequat. Pellentesque faucibus tincidunt augue non consequat. Donec fringilla at est sit amet blandit. Nunc at porttitor ligula. Fusce sed odio turpis."},
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
