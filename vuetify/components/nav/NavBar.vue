<template>
  <v-navigation-drawer theme="dark" width="80" permanent>
    <div class="d-flex flex-column align-center h-100 justify-space-around">
      <v-icon :icon="mdiHome" />
      <v-icon :icon="mdiFilm" />
      <v-icon :icon="mdiTelevision" />
      <v-icon :icon="mdiTextSearchVariant" />
    </div>
  </v-navigation-drawer>
</template>

<script setup>
import { mdiHome, mdiFilm, mdiTelevision, mdiTextSearchVariant } from "@mdi/js";
</script>
<style lang="csss" scoped></style>
