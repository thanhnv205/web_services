<template>
  <section class="wrapper">
    <div class="roration">
      <div class="roration-circle">
        <div class="roration-luck" :style="{ transform: `rotate(${data}deg)` }">
          <div attr="1" class="luck-item">
            <svg>
              <g stroke="white">
                <path
                  fill="rgb(93, 180, 172)"
                  d="M1.5308084989341916e-14,-250A250,250,0,0,1,135.16020436389942,-210.31338320779528L0,0Z"
                ></path>
              </g>
            </svg>
          </div>
          <div attr="2" class="luck-item">
            <svg>
              <g stroke="white">
                <path
                  fill="rgb(93, 180, 172)"
                  d="M1.5308084989341916e-14,-250A250,250,0,0,1,135.16020436389942,-210.31338320779528L0,0Z"
                ></path>
              </g>
            </svg>
          </div>
          <div attr="3" class="luck-item">
            <svg>
              <g stroke="white">
                <path
                  fill="rgb(93, 180, 172)"
                  d="M1.5308084989341916e-14,-250A250,250,0,0,1,135.16020436389942,-210.31338320779528L0,0Z"
                ></path>
              </g>
            </svg>
          </div>
          <div attr="4" class="luck-item">
            <svg>
              <g stroke="white">
                <path
                  fill="rgb(93, 180, 172)"
                  d="M1.5308084989341916e-14,-250A250,250,0,0,1,135.16020436389942,-210.31338320779528L0,0Z"
                ></path>
              </g>
            </svg>
          </div>
          <div attr="5" class="luck-item">
            <svg>
              <g stroke="white">
                <path
                  fill="rgb(93, 180, 172)"
                  d="M1.5308084989341916e-14,-250A250,250,0,0,1,135.16020436389942,-210.31338320779528L0,0Z"
                ></path>
              </g>
            </svg>
          </div>
          <div attr="6" class="luck-item">
            <svg>
              <g stroke="white">
                <path
                  fill="rgb(93, 180, 172)"
                  d="M1.5308084989341916e-14,-250A250,250,0,0,1,135.16020436389942,-210.31338320779528L0,0Z"
                ></path>
              </g>
            </svg>
          </div>
          <div attr="7" class="luck-item">
            <svg>
              <g stroke="white">
                <path
                  fill="rgb(93, 180, 172)"
                  d="M1.5308084989341916e-14,-250A250,250,0,0,1,135.16020436389942,-210.31338320779528L0,0Z"
                ></path>
              </g>
            </svg>
          </div>
          <div attr="8" class="luck-item">
            <svg>
              <g stroke="white">
                <path
                  fill="rgb(93, 180, 172)"
                  d="M1.5308084989341916e-14,-250A250,250,0,0,1,135.16020436389942,-210.31338320779528L0,0Z"
                ></path>
              </g>
            </svg>
          </div>
        </div>
      </div>
      <div class="roration-arrow" />
    </div>

    <div class="roration-footer">
      <button class="text-white btn-game" @click="spinWheel">Start</button>
    </div>
  </section>
</template>

<script setup>
import { ref } from "vue";
const data = ref(0);

const getPosition = (position) => {
  console.log("position", position);
  if (position <= 360) {
    console.log(8);
  } else if (position <= 315) {
    console.log(7);
  } else if (position <= 270) {
    console.log(6);
  } else if (position <= 225) {
    console.log(5);
  } else if (position <= 180) {
    console.log(4);
  } else if (position <= 135) {
    console.log(3);
  } else if (position <= 90) {
    console.log(2);
  } else if (position <= 45) {
    console.log(1);
  }
};

const spinWheel = () => {
  const randomRotation = Math.floor(Math.random() * (720 - 360 + 1) + 360);
  console.log("randomRotation", randomRotation);
  data.value += randomRotation;
  setTimeout(() => {
    getPosition(data.value % 360);
  }, 5000);
};
</script>

<style scoped lang="scss">
.wrapper {
  width: 100vw;
  height: 100vh;
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
    width: 400px;
    height: 400px;
    border: 15px solid #610000;
    border-radius: 50%;
    box-sizing: content-box;
    .roration-luck {
      width: 100%;
      height: 100%;
      border-radius: 100%;
      overflow: hidden;
      transition: transform 4s ease-in-out;
      display: flex;
      justify-content: center;

      .luck-item {
        position: absolute;
        width: 0;
        height: 0;
        border-left: 83px solid transparent;
        border-right: 83px solid transparent;
        border-top: 200px solid #ea4b4c;
        transform-origin: 50% 100%;
      }
    }

    .luck-item:nth-child(1) {
      border-top-color: #16a085;
      transform: rotate(360deg);
    }
    .luck-item:nth-child(2) {
      border-top-color: red;
      transform: rotate(315deg);
    }
    .luck-item:nth-child(3) {
      border-top-color: #16a085;
      transform: rotate(270deg);
    }
    .luck-item:nth-child(4) {
      border-top-color: red;
      transform: rotate(225deg);
    }

    .luck-item:nth-child(5) {
      border-top-color: #16a085;
      transform: rotate(180deg);
    }
    .luck-item:nth-child(6) {
      border-top-color: red;
      transform: rotate(135deg);
    }

    .luck-item:nth-child(7) {
      border-top-color: #16a085;
      transform: rotate(90deg);
    }
    .luck-item:nth-child(8) {
      border-top-color: red;
      transform: rotate(45deg);
    }
  }
  &-arrow {
    position: absolute;
    top: -20px;
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-right: 50px solid transparent;
    border-top: 100px solid #ea4b4c;
    border-radius: 50px;
    &::before {
      content: "";
      content: "";
      position: absolute;
      top: -145px;
      left: -48px;
      width: 100px;
      height: 50px;
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
