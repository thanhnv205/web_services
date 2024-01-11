<template>
  <div class="title-comp">
    <h1 class="heading-section" :class="[`arrow-${line}`]">
      {{ title }}
    </h1>
    <h3 class="description-section">{{ description }}</h3>
  </div>
</template>

<script setup>
const { title, description, line } = defineProps([
  "title",
  "description",
  "line",
]);
</script>

<style scoped>
.title-comp {
  margin-bottom: 25px;
}
.heading-section {
  position: relative;
  width: fit-content;
  font-size: 18px;
  font-weight: 600;
  display: flex;
  align-items: center;
}

.heading-section::before {
  content: "";
  position: absolute;
  width: var(--width-line-title);
  height: 2px;
  background-color: #000;
}
.arrow-right::before {
  left: calc(var(--width-line-title) + 20px);
}
.arrow-left {
  left: calc(var(--width-line-title) + 20px);
}
.arrow-left::before {
  right: calc(var(--width-line-title) + 20px);
}
.description-section {
  margin-top: 25px;
  font-size: 48px;
  font-weight: 700;
}
</style>
