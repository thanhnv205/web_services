<template>
  <section class="section">
    <TitleSection
      title="Services"
      description="Our capacity to help make your wishes come true"
      line="right"
    />
  </section>

  <section class="service clear-space">
    <v-row no-gutters class="font-0 custom-row">
      <v-col cols="4">
        <div class="spacing-x">
          <div class="service-img">
            <img src="~/assets/images/service-1.png" alt="" />
          </div>
          <div class="service-text">Interior Design</div>
        </div>
      </v-col>
      <v-col cols="4">
        <div class="spacing-x">
          <div class="service-img">
            <img src="~/assets/images/service-2.png" alt="" />
          </div>
          <div class="service-text">Architecture</div>
        </div>
      </v-col>
      <v-col cols="4">
        <div class="spacing-x">
          <div class="service-img">
            <img src="~/assets/images/service-3.png" alt="" />
          </div>
          <div class="service-text">Furniture Design</div>
        </div>
      </v-col>
    </v-row>
  </section>
</template>

<style scoped>
.custom-row {
  margin: 0 -5px;
}
.spacing-x {
  position: relative;
  padding: 0 calc(5px / 2);
}
.service-text {
  position: absolute;
  bottom: 25px;
  left: 35px;
  color: var(--color-white);
  font-size: 24px;
  font-weight: 700;
  letter-spacing: 0.48px;
  text-transform: capitalize;
  line-height: 1.2;
}
</style>
