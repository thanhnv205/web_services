<template>
  <section class="section">
    <TitleSection
      title="Our Blog"
      description="Latest News and Articles"
      line="right"
    />
  </section>

  <section class="our-blog">
    <v-row no-gutters class="font-0 custom-row">
      <v-col cols="4">
        <div class="spacing-x">
          <div class="our-blog-img d-flex flex-column">
            <img class="w-100" src="~/assets/images/blog-img-3.png" alt="" />
            <p class="author-img">Interior Design</p>
          </div>

          <div class="our-blog-more">
            <h4 class="our-blog-title">Designer must be an interpreter</h4>
            <p class="our-blog-desc">
              Lorem ipsum dolor sit amet, conse ctetur adipiscing elit.
              Adipiscing dui tellus commodo convallis. Auctor eget orci pharetra
              non Adipiscing dui tellus commodo convallis. Auctor eget orci
              pharetra non
            </p>
          </div>
        </div>
      </v-col>

      <v-col cols="4">
        <div class="spacing-x">
          <div class="our-blog-img d-flex flex-column">
            <img class="w-100" src="~/assets/images/blog-img-2.png" alt="" />
            <p class="author-img">Interior Design</p>
          </div>

          <div class="our-blog-more">
            <h4 class="our-blog-title">Designer must be an interpreter</h4>
            <p class="our-blog-desc">
              Lorem ipsum dolor sit amet, conse ctetur adipiscing elit.
              Adipiscing dui tellus commodo convallis. Auctor eget orci pharetra
              non Adipiscing dui tellus commodo convallis. Auctor eget orci
              pharetra non
            </p>
          </div>
        </div>
      </v-col>

      <v-col cols="4">
        <div class="spacing-x">
          <div class="our-blog-img d-flex flex-column">
            <img class="w-100" src="~/assets/images/blog-img-1.png" alt="" />
            <p class="author-img">Interior Design</p>
          </div>

          <div class="our-blog-more">
            <h4 class="our-blog-title">Designer must be an interpreter</h4>
            <p class="our-blog-desc">
              Lorem ipsum dolor sit amet, conse ctetur adipiscing elit.
              Adipiscing dui tellus commodo convallis. Auctor eget orci pharetra
              non Adipiscing dui tellus commodo convallis. Auctor eget orci
              pharetra non
            </p>
          </div>
        </div>
      </v-col>
    </v-row>
  </section>
</template>

<style lang="scss" scoped>
.custom-row {
  margin: 0 -25px;
}
.spacing-x {
  padding: 0 25px;
}
.author-img {
  margin: 10px 0;
  color: var(--color-secondary);
  font-size: 18px;
  font-weight: 600;
  letter-spacing: 0.36px;
  text-transform: capitalize;
}
.our-blog {
  &-title {
    color: var(--color-black);
    font-size: 32px;
    font-weight: 700;
    line-height: 42px;
    letter-spacing: 0.64px;
  }
  &-desc {
    margin-top: 25px;
    font-family: var(--font-secondary);
    color: var(--color-secondary);
    font-size: 16px;
    font-weight: 500;
    line-height: 20px;
  }
}
.our-blog-info {
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
