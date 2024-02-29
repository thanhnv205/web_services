<template>
  <v-container class="container">
    <v-app>
      <v-main>
        <slot />
      </v-main>
    </v-app>
  </v-container>
</template>

<style scoped>
.container {
  margin: 0px auto;
  padding: 0px;
  width: 1440px;
}
</style>
