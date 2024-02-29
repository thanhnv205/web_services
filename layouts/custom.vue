<template>
  <v-app>
    <v-main class="custom-main">
      <slot />
    </v-main>
  </v-app>
</template>

<style scoped>
.custom-main {
  width: 100vw;
  height: 100vh;
  padding: 0;
}
</style>
