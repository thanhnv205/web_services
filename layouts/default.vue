<template>
  <v-container class="container">
    <v-app>
      <Header />

      <v-main>
        <slot />
      </v-main>
      <Footer />
    </v-app>
  </v-container>
</template>

<script setup>
import Header from "~/vuetify/components/Header.vue";
import Footer from "~/vuetify/components/Footer.vue";
</script>

<style scoped>
.container {
  margin: 0px auto;
  padding: 0px;
  width: 1440px;
}
</style>
