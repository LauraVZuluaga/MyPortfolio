<template>
  <div>
    <section class="about-section sec-padding">
      <div class="container">
        <div class="row">
          <div class="section-title">
            <h2>About me</h2>
          </div>
        </div>
        <div class="row">
          <div class="about-img">
            <div class="">
              <img src="@/assets/about(2).png" alt="about image" />
            </div>
          </div>
          <div class="about-text">
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Facilis,
              minus fugiat excepturi odit eligendi quam necessitatibus ullam
              recusandae facere distinctio tenetur repellat hic totam
              consequuntur qui dolorem eveniet, eum molestias!
            </p>
            <h3>Skills</h3>
            <div class="skills">
              <div class="skill-item">HTML</div>
              <div class="skill-item">CSS</div>
              <div class="skill-item">JavaScript</div>
              <div class="skill-item">VueJs</div>
              <div class="skill-item">Bootstrap</div>
            </div>
            <div class="about-tabs">
              <app-button
                type="button"
                class="tab-item"
                :class="disabled ? 'active' : ''"
                v-on:click="seeInfo"
                >Education </app-button
              >
              <app-button
                type="button"
                class="tab-item"
                :class="!disabled ? 'active' : ''"
                v-on:click="seeInfo"
                >Experience</app-button
              >
            </div>

            <!------ Education Section ----->
            <div class="tab-content" id="education" v-if="disabled">
              <div class="timeline">
                <div class="timeline-item">
                  <span class="date"> 2016 - 2021 </span>
                  <h4>
                    Computer and Systems Engineering -
                    <span> Universidad de Caldas </span>
                  </h4>
                  <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Iusto quas dolore expedita exercitationem tempore beatae
                    pariatur, ad unde eligendi sit tenetur reprehenderit
                    deleniti asperiores? Maiores ex sit voluptatum doloribus
                    nulla?
                  </p>
                </div>
                <div class="timeline-item">
                  <span class="date"> 2015 </span>
                  <h4>
                    Academic Degree -
                    <span> Escuela Superior de Manizales </span>
                  </h4>
                  <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Iusto quas dolore expedita exercitationem tempore beatae
                    pariatur, ad unde eligendi sit tenetur reprehenderit
                    deleniti asperiores? Maiores ex sit voluptatum doloribus
                    nulla?
                  </p>
                </div>
              </div>
            </div>
            <!------ End Education Section ----->

            <!------- Experience Section -------->
            <div class="tab-content" id="experience" v-if="!disabled">
              <div class="timeline">
                <div class="timeline-item">
                  <span class="date"> 2020 - Now </span>
                  <h4>
                    Frontend Developer -
                    <span> TEK Soluciones Tecnológicas </span>
                  </h4>
                  <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Iusto quas dolore expedita exercitationem tempore beatae
                    pariatur, ad unde eligendi sit tenetur reprehenderit
                    deleniti asperiores? Maiores ex sit voluptatum doloribus
                    nulla?
                  </p>
                </div>
                <div class="timeline-item">
                  <span class="date"> 2019 - 2020 </span>
                  <h4>
                    Frontend Developer -
                    <span> Universidad de Caldas </span>
                  </h4>
                  <p>
                    Lorem ipsum dolor sit amet consectetur, adipisicing elit.
                    Iusto quas dolore expedita exercitationem tempore beatae
                    pariatur, ad unde eligendi sit tenetur reprehenderit
                    deleniti asperiores? Maiores ex sit voluptatum doloribus
                    nulla?
                  </p>
                </div>
              </div>
            </div>
            <!------- End Experience Section -------->
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "app-info",
  data() {
    return {
      disabled: true,
    };
  },
  methods: {
    seeInfo() {
      this.disabled ? (this.disabled = false) : (this.disabled = true);
      console.log(this.disabled, "información de disabled");
    },
  },
};
</script>

<style></style>
