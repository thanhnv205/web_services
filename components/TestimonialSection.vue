<template>
  <section class="section">
    <TitleSection
      title="Testimonial"
      description="What Our Clients Say"
      line="right"
    />
  </section>

  <section class="testimonial">
    <v-row no-gutters class="font-0 custom-row">
      <v-col cols="4">
        <div class="spacing-x">
          <div class="testimonial-item">
            <div class="testimonial-user d-flex align-center">
              <img src="~/assets/images/avata-1.png" alt="" />

              <div class="testimonial-info">
                <h3 class="client-name">Menta Nia</h3>
                <span class="client-company">Company Name</span>
              </div>
            </div>

            <div class="testimonial-more">
              <p>
                “ Lorem ipsum dolor sit amet, conse ctetur adipiscing elit.
                Adipiscing dui tellus commodo convallis. Auctor eget orci
                pharetra non Adipiscing dui tellus commodo convallis. Auctor
                eget orci pharetra non “
              </p>
            </div>
          </div>
        </div>
      </v-col>
      <v-col cols="4">
        <div class="spacing-x">
          <div class="testimonial-item">
            <div class="testimonial-user d-flex align-center">
              <img src="~/assets/images/avata-2.png" alt="" />

              <div class="testimonial-info">
                <h3 class="client-name">Menta Nia</h3>
                <span class="client-company">Company Name</span>
              </div>
            </div>

            <div class="testimonial-more">
              <p>
                “ Lorem ipsum dolor sit amet, conse ctetur adipiscing elit.
                Adipiscing dui tellus commodo convallis. Auctor eget orci
                pharetra non Adipiscing dui tellus commodo convallis. Auctor
                eget orci pharetra non “
              </p>
            </div>
          </div>
        </div>
      </v-col>
      <v-col cols="4">
        <div class="spacing-x">
          <div class="testimonial-item">
            <div class="testimonial-user d-flex align-center">
              <img src="~/assets/images/avata-3.png" alt="" />

              <div class="testimonial-info">
                <h3 class="client-name">Menta Nia</h3>
                <span class="client-company">Company Name</span>
              </div>
            </div>

            <div class="testimonial-more">
              <p>
                “ Lorem ipsum dolor sit amet, conse ctetur adipiscing elit.
                Adipiscing dui tellus commodo convallis. Auctor eget orci
                pharetra non Adipiscing dui tellus commodo convallis. Auctor
                eget orci pharetra non “
              </p>
            </div>
          </div>
        </div>
      </v-col>
    </v-row>
  </section>
</template>

<style scoped>
.custom-row {
  margin: 0 -25px;
}
.spacing-x {
  padding: 0 25px;
}
.testimonial-item {
  padding: 40px;
  background-color: var(--bg-secondary-color);
}
.testimonial-user {
  margin-bottom: 40px;
}
.testimonial-info {
  margin-left: 15px;
  text-transform: capitalize;
}
.client-name {
  font-size: 18px;
  font-weight: 700;
  letter-spacing: 0.36px;
  line-height: 1.2;
  margin-bottom: 5px;
}
.client-company {
  color: #3d3d3d;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 0.28px;
}
</style>
