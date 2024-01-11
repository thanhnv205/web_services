<template>
  <!-- <section class="section">
    <TitleSection
      title="Our Project"
      description="Our latest projects"
      line="right"
    />
  </section> -->

  <section class="section">
    <v-row no-gutters>
      <v-col cols="6">
        <v-row no-gutters>
          <v-col cols="6">
            <img src="~/assets/images/partner-2.png" alt="" />
          </v-col>
          <v-col cols="6">
            <img src="~/assets/images/partner-1.png" alt="" />
          </v-col>
        </v-row>

        <div class="into-achieve">
          <v-row no-gutters>
            <v-col cols="4">
              <div class="item-achieve">
                <b class="achieve-number w-100 d-block text-center">10</b>
                <span class="achieve-desc text-center d-block">Years</span>
              </div>
            </v-col>
            <v-col cols="4">
              <div class="item-achieve">
                <b class="achieve-number w-100 d-block text-center">200+</b>
                <span class="achieve-desc text-center d-block">Project</span>
              </div>
            </v-col>
            <v-col cols="4">
              <div class="item-achieve">
                <b class="achieve-number w-100 d-block text-center">80</b>
                <span class="achieve-desc text-center d-block">Partners</span>
              </div>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="6">
        <div class="intro-right">
          <TitleSection
            title="Hello There"
            line="left"
            description="We work professionally and wholeheartedly"
          />
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Adipiscing
            dui tellus commodo convallis. Auctor eget orci pharetra non. Integer
            lorem in scelerisque tortor dui tempor, volutpat viverra faucibus.
            Sagittis maecenas tincidunt at purus. Amet non vel elit aliquet id
            dolor risus imperdiet vitae. Amet, sagittis mauris morbi erat velit
            id nullam. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
            Adipiscing dui tellus commodo convallis.
          </p>
        </div>
      </v-col>
    </v-row>
  </section>
</template>

<style scoped>
.intro-right {
  padding: 70px;
}

.into-achieve {
  width: 65%;
  margin-left: auto;
  background: var(--bg-secondary-color);
  box-shadow: 5px 5px 10px 0px rgba(0, 0, 0, 0.05);
}
.item-achieve {
  position: relative;
  padding: 30px 40px;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}
.achieve-number {
  font-size: 36px;
  line-height: 1.2;
}
.achieve-desc {
  font-size: 18px;
  font-weight: 600;
}
.v-col-4:not(:first-child) .item-achieve::after {
  position: absolute;
  content: "";
  width: 1px;
  left: 0;
  height: 60px;
  background-color: #3d3d3d;
}
</style>
