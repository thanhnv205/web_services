<template>
  <section class="section">
    <TitleSection
      title="Our Project"
      description="Our latest projects"
      line="right"
    />
  </section>

  <section class="our-project">
    <div class="Our latest projects-img clear-space">
      <img src="~/assets/images/our-banner.png" alt="" />
    </div>

    <div class="project-content">
      <h3 class="project-content-title">Hanani Home</h3>
      <span class="project-content-desc"
        >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Adipiscing dui
        tellus commodo convallis. Auctor eget orci pharetra non.
      </span>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.our-project {
  position: relative;
}
.project-content {
  position: absolute;
  max-width: 376px;
  bottom: 0;
  padding: 50px;
  color: var(--color-white);
  &-title {
    font-size: 24px;
    font-weight: 600;
    letter-spacing: 0.48px;
    text-transform: capitalize;
    margin-bottom: 25px;
    line-height: 1;
  }
  &-desc {
    font-family: var(--font-secondary);
    font-size: 16px;
    font-weight: 300;
  }
}
</style>
