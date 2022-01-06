<template>
  <div class="main">
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
              Hello, again! I am (almost... I'm looking forward to my
              graduation, how exciting) a Systems Engineer dedicated to frontend
              development. Making people happy through technology is an honor
              😊, and I'm from Colombia. I love reading, dancing, laughing,
              spending time with the people I love and learning new things.
            </p>
            <br />
            <p>
              ¡Hola, de nuevo! Soy (casi... estoy esperando mi graduación, qué
              emocionante) una Ingeniera de Sistemas, dedicado al desarrollo
              frontend. Hacer feliz a la gente a través de la tecnología es un
              honor 😊, y soy de Colombia. Me encanta leer, bailar, reír, pasar
              tiempo con las personas que quiero y aprender cosas nuevas.
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
                >Education
              </app-button>
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
                    My training as an engineer and programmer started here. It
                    has not been an easy path, but Systems Engineering changed
                    my way of seeing the world, and I am happy with that. My
                    greatest desire is to help people to have a better quality
                    of life through technology.
                  </p>
                  <br />
                  <p>
                    Mi formación como ingeniera y programadora comenzó aquí. No
                    ha sido un camino fácil, pero la Ingeniería de Sistemas
                    cambió mi forma de ver el mundo, y estoy contenta con ello.
                    Mi mayor deseo es ayudar a las personas a tener una mejor
                    calidad de vida a través de la tecnología.
                  </p>
                </div>
                <div class="timeline-item">
                  <span class="date"> 2015 </span>
                  <h4>
                    Academic Degree -
                    <span> Escuela Superior de Manizales </span>
                  </h4>
                  <p>
                    The school's mission is to train teachers for elementary
                    school children. I learned not only what it takes to get
                    into college, but the magic and importance of not giving up
                    being a kid at heart even as the years go by.
                  </p>
                  <br />
                  <p>
                    La misión de la escuela es formar profesores para niños de
                    primaria. Aprendí no sólo lo que se necesita para entrar en
                    la universidad, sino la magia y la importancia de no dejar
                    de ser un niño de corazón aunque pasen los años.
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
                    My first real-world experience with VueJS. Creating a custom
                    CRM is quite a challenge and even more so in a company that
                    has areas with such different tasks. I have learned a lot
                    about the framework, user experience and teamwork.
                  </p>
                  <br />
                  <p>
                    Mi primera experiencia en el mundo real con VueJS. Crear un
                    CRM a la medida es todo un reto y más en una empresa que
                    tiene áreas con tareas tan diferentes. He aprendido
                    muchísimo del framework, de la experiencia de usuario y el
                    trabajo en equipo.
                  </p>
                </div>
                <div class="timeline-item">
                  <span class="date"> 2019 - 2020 </span>
                  <h4>
                    Frontend Developer -
                    <span> Universidad de Caldas </span>
                  </h4>
                  <p>
                    My main tool was WordPress, however, for the same reason I
                    had to learn HTML, CSS and Javascript, templates limit your
                    possibilities. Also, I attended meetings with clients to
                    understand their needs; I helped create a small agile
                    methodology system, based on agilUC, and I learned a lot
                    from it.
                  </p>
                  <br />
                  <p>
                    Mi herramienta principal era WordPress, sin embargo, por la
                    misma razón tuve que aprender HTML, CSS y Javascript, las
                    plantillas te limitan las posibilidades. También, asistía a
                    las reuniones con clientes para entender sus necesidades;
                    ayudé a crear un pequeño sistema de metodología ágil, basado
                    en agilUC, y aprendí mucho de ello.
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
