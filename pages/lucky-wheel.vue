<template>
  <section class="wrapper">
    <div class="roration">
      <div class="roration-circle wheel">
        <div
          class="roration-luck"
          :style="{ transform: `rotate(${rotation}deg)` }"
          ref="rotationLuck"
        >
          <div
            class="luck-item"
            v-for="(section, index) in sections"
            :key="index"
            :style="{
              color: '#fff',
              backgroundColor: section.color,
              transform: `rotate(${index * (360 / sections.length)}deg)`,
              width: `${calculateWidth(sections.length)}px`,
            }"
          >
            {{ section.value }}
          </div>
        </div>
      </div>
      <div class="roration-arrow" />
    </div>

    <div class="roration-footer">
      <button class="text-white btn-game" @click="startSpinning">Start</button>
    </div>
    <p v-if="winningPosition !== null">
      Giải thưởng trúng tại vị trí {{ winningPosition }}
    </p>
  </section>
</template>

<script setup>
import { ref, onUnmounted } from "vue";

definePageMeta({
  layout: "custom",
});

const sections = ref([
  { value: 1, color: "red" },
  { value: 2, color: "green" },
  { value: 3, color: "red" },
  { value: 4, color: "green" },
  { value: 5, color: "red" },
  { value: 6, color: "green" },
  { value: 7, color: "red" },
  { value: 8, color: "green" },
  { value: 9, color: "red" },
  { value: 10, color: "green" },
]);

const calculateWidth = (number) => {
  const wheelRadius = 220;
  return Math.floor((2 * Math.PI * wheelRadius) / number);
};

const winningPosition = ref(null);
const rotation = ref(0);
let intervalId = null;

const getRandomInt = (time) => {
  const max = Math.floor(time);
  const min = Math.ceil(time - 360);
  return Math.floor(Math.random() * (max - min)) + min;
};

const startSpinning = () => {
  const d = 2 * Math.PI * 220;
  const part = 360 / sections.value.length;

  sections.value = sections.value.map((item, index) => ({
    ...item,
    transform_start: index * Math.floor(d / sections.value.length - part / 2),
    transform_end: index * Math.floor(d / sections.value.length + part / 2),
  }));

  const totalTime = getRandomInt(1000);
  const startRun = 20;
  const endRun = 1;

  winningPosition.value = null;

  let currentRotation = 0;
  let currentSpeed = startRun;
  currentRotation += currentSpeed;
  rotation.value = 360;

  intervalId = setInterval(() => {
    currentRotation += currentSpeed;
    rotation.value = currentRotation;
    if (currentRotation >= totalTime) {
      clearInterval(intervalId);
      setPositionPrize(currentRotation);
    } else if (totalTime - currentRotation <= 1) {
      const progress = currentRotation / totalTime;
      currentSpeed = startRun + (0.3 - startRun) * progress;
    } else {
      const progress = currentRotation / totalTime;
      currentSpeed = startRun + (endRun - startRun) * progress;
    }
  }, 16);
};

onUnmounted(() => clearInterval(intervalId));

const setPositionPrize = (currentRotation) => {
  const amoutOptions = sections.value.length;
  const d = 2 * Math.PI * 220;
  const degreesPerOption = d / amoutOptions;

  const relativeRotation = Math.floor(currentRotation % d);
  const winningSector = Math.floor(relativeRotation / degreesPerOption);
  console.log(currentRotation);
};
</script>

<style scoped lang="scss">
.wrapper {
  display: flex;
  flex-flow: column;
  align-items: center;
  height: 100%;
  padding-top: 10%;
  background-image: url("../assets/images/lucky-wrapper.jpg");
  background-size: cover;
}

.roration {
  position: relative;
  width: 500px;
  height: 500px;
  display: flex;
  justify-content: center;
  background-image: url("~/assets/images/border-wheel.png");
  background-size: 100%;
  align-items: center;

  &-circle {
    position: relative;
    border: 2px solid #fff;
    border-radius: 50%;
    box-sizing: border-box;

    .roration-luck {
      width: 420px;
      height: 420px;
      display: flex;
      align-items: baseline;
      justify-content: center;
      overflow: hidden;
      clip-path: circle(50% at 50% 50%);

      .luck-item {
        position: absolute;
        height: 210px;
        font-size: 50px;
        text-align: center;
        clip-path: polygon(50% 100%, 0 0, 100% 0);
        transform-origin: 50% 100%;
      }
    }
  }

  &-arrow {
    position: absolute;
    top: 5px;
    width: 80px;
    height: 90px;
    clip-path: polygon(50% 100%, 100% 18%, 75% 0, 25% 0, 0 18%);
    background-color: #610000;
  }

  &-footer {
    margin-top: 50px;
  }
}

.btn-game {
  font-size: 20px;
  padding: 10px 70px;
  border-radius: 15px;
  background-image: linear-gradient(0deg, #e20000, #f39696 0%, #e20000);
  border: 2px solid #f39696;
  transition: 0.5s ease-in-out;

  &:not(:hover) {
    box-shadow: 0 10px 10px -7px #610000;
  }

  &:hover {
    transform: translateY(5px);
  }
}
</style>
