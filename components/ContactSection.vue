<template>
  <section class="section">
    <div class="contact">
      <div class="contact-content">
        <h3 class="contact-heading">
          Have A Question ? Start Consultation Now
        </h3>
        <p class="contact-desc">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Adipiscing
          dui tellus commodo convallis.
        </p>

        <v-btn
          text="contact-us"
          class="btn bg-black text-white rounded-0"
          size="x-large"
        >
          <template v-slot:append>
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M7 17L17 7"
                stroke="white"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M7 7H17V17"
                stroke="white"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </template>
        </v-btn>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.contact {
  background-image: url("~/assets/images/contact-home.png");
  background-size: cover;
  &-content {
    max-width: 700px;
    padding: 90px 100px;
  }
  &-heading {
    color: var(--color-secondary);
    font-size: 40px;
    font-weight: 700;
    line-height: 54px;
    letter-spacing: 0.8px;
    text-transform: capitalize;
  }
  &-desc {
    margin: 25px 0;
    color: var(--color-secondary);
    font-family: var(--font-secondary);
    font-size: 16px;
    font-weight: 500;
    line-height: 20px;
  }
}
</style>
