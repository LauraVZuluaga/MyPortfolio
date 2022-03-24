<template>
  <div class="main">
    <section class="home-section aling-items-center">
      <div class="container">
        <div class="row aling-items-center">
          <div class="home-text">
            <p>Hello, I'm</p>
            <h1>Laura Zuluaga</h1>
            <h2>Frontend Developer</h2>
            <p
              style="margin-bottom: 21px !important; font-size: 12px !important"
            >
              (Sorry for the inconvenience, I am modifying the project with
              Tailwind for a better experience).
            </p>
            <a href="#" class="btn"
              ><router-link :to="{ name: 'About' }"
                >More about me
              </router-link></a
            >
            <a href="#" class="btn"
              ><router-link :to="{ name: 'Portfolio' }"
                >Portfolio
              </router-link></a
            >
          </div>
          <div class="home-img">
            <div class="">
              <img src="@/assets/programmer6.png" alt="programmer-img" />
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "app-home-portfolio",
};
</script>

<style lang="scss"></style>
