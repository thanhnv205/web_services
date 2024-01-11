<template>
  <v-container class="container">
    <v-app>
      <Header />
      <!-- <NavBar /> -->
      <v-main>
        <slot />
      </v-main>
    </v-app>
  </v-container>
</template>

<script setup>
import Header from "~/vuetify/components/Header.vue";
</script>

<style scoped>
.container {
  margin: 0px auto;
  padding: 0px;
  width: 1440px;
}
</style>
