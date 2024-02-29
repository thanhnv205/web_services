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
            :class="{ winner: index + 1 === winningPosition }"
            :style="{
              color: '#fff',
              backgroundColor: section.color,
              transform: `rotate(${index * (360 / sections.length)}deg)`,
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

const sections = [
  { value: 1, color: "red" },
  { value: 2, color: "green" },
  { value: 3, color: "red" },
  { value: 4, color: "green" },
  { value: 5, color: "red" },
  { value: 6, color: "green" },
  { value: 7, color: "red" },
  { value: 8, color: "green" },
];

const winningPosition = ref(null);
const rotation = ref(0);
let intervalId = null;

const startSpinning = () => {
  const totalTime = 3000;
  const startRun = 10;
  const endRun = 1;

  winningPosition.value = null;

  let currentRotation = 0;
  let currentSpeed = startRun;

  const getRandomInt = (min, max) => {
    const minCeiled = Math.ceil(min);
    const maxFloored = Math.floor(max);
    return Math.floor(Math.random() * (maxFloored - minCeiled + 1) + minCeiled);
  };
  const generatedPosition = getRandomInt(1, totalTime);
  // const updateRotation = () => {
  //   currentRotation += randomPieMovement;
  //   rotation.value = currentRotation;

  //   if (currentRotation >= randomPieMovement) {
  //     clearInterval(intervalId);
  //     determineWinningPosition();
  //   } else if (randomPieMovement - currentRotation <= 1) {
  //     const progress = currentRotation / randomPieMovement;
  //     currentSpeed = startRun + (0.3 - startRun) * progress;
  //   } else {
  //     const progress = currentRotation / randomPieMovement;
  //     currentSpeed = startRun + (endRun - startRun) * progress;
  //   }
  // };
  console.log("updateRotation", updateRotation);
  // intervalId = setInterval(updateRotation, 10);
  onUnmounted(() => clearInterval(intervalId));
};

const determineWinningPosition = () => {
  const numberOfOptions = sections.length;
  const degreesPerSpin = 360;
  const winningSector = Math.floor(
    rotation.value / (degreesPerSpin / numberOfOptions)
  );

  winningPosition.value = sections[winningSector % numberOfOptions].value;
};
</script>
<style scoped lang="scss">
.wrapper {
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
}
.roration {
  position: relative;
  display: flex;
  justify-content: center;
  &-circle {
    position: relative;
    border: 15px solid #610000;
    border-radius: 50%;
    box-sizing: border-box;
    .roration-luck {
      width: 400px;
      height: 400px;
      display: flex;
      align-items: baseline;
      justify-content: center;
      overflow: hidden;
      clip-path: circle(50% at 50% 50%);

      .luck-item {
        position: absolute;
        width: 160px;
        height: 200px;
        font-size: 50px;
        text-align: center;
        clip-path: polygon(50% 100%, 0 0, 100% 0);
        transform-origin: 50% 100%;
      }
    }
  }
  &-arrow {
    position: absolute;
    top: -20px;
    width: 0;
    height: 0;
    border-left: 40px solid transparent;
    border-right: 40px solid transparent;
    border-top: 80px solid #ea4b4c;
    border-radius: 50px;
    &::before {
      content: "";
      position: absolute;
      top: -95px;
      left: -48px;
      width: 80px;
      height: 20px;
      background-color: #fff;
    }
  }

  &-footer {
    margin-top: 50px;
  }
}
.btn-game {
  font-size: 20px;
  padding: 10px 50px;
  border-radius: 15px;
  background-image: linear-gradient(0deg, #ea4b4c, #f39696 0%, #ea4b4c);
  border: 2px solid #f39696;
  transition: all 0.5s;
  &:not(:hover) {
    box-shadow: 0 10px 10px -7px red;
  }
  &:hover {
    transform: translateY(5px);
  }
}
</style>
