<template>
  <section class="hero pt-10">
    <v-row no-gutters>
      <v-col cols="6">
        <div class="hero-content">
          <h2 class="hero-title">
            Create a modern and unique design your dream
          </h2>
          <p class="hero-desc">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Adipiscing
            dui tellus commodo convallis. Auctor eget orci pharetra non. Integer
            lorem in scelerisque tortor dui tempor
          </p>
          <v-btn
            to="/"
            variant="outlined"
            color="#000"
            size="x-large"
            class="btn-transparent btn text-none"
          >
            View more
            <template v-slot:append>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
              >
                <path
                  d="M5 12H19"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M12 5L19 12L12 19"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </template>
          </v-btn>
        </div>
      </v-col>
      <v-col cols="6">
        <img src="~/assets/images/hero.png" alt="Banner" />
      </v-col>
    </v-row>
  </section>
</template>

<style type="scss" scoped>
.hero-content {
  padding: 60px 60px 30px 100px;
}
.hero-title {
  font-size: 52px;
  letter-spacing: 1.04px;
  line-height: 1.2;
  margin-bottom: 35px;
}
.hero-desc {
  font-size: 18px;
  font-weight: 500;
  line-height: 24px;
  margin-bottom: 50px;
}
img {
  object-fit: cover;
  height: 100%;
}
</style>
