<template>
  <div class="main">
    <section class="portfolio-section sec-padding">
      <div class="container">
        <div class="row">
          <div class="section-title">
            <h2>Recent Work</h2>
          </div>
        </div>

        <div class="row">
          <!------- Portfolio Items --------->
          <div
            class="portfolio-item"
            v-for="projectInfo in this.projectsInfo"
            :key="projectInfo.id"
          >
            <div class="portfolio-item-thumbnail">
              <img :src="projectInfo.image" alt="portfolio item thumb" />
            </div>
            <h3 class="portfolio-item-title">{{ projectInfo.name }}</h3>
            <div class="portfolio-item-details">
              <div class="pp-body">
                <div class="description">
                  <p>
                    {{ projectInfo.englishDescription }}
                  </p>
                  <br />
                  <p>
                    {{ projectInfo.spanishDescription }}
                  </p>
                </div>
                <div class="general-info">
                  <ul>
                    <li>
                      Created - <span> {{ projectInfo.createdAt }} </span>
                    </li>
                    <li>
                      Tecnologies used -
                      <span> {{ projectInfo.tecnologies }} </span>
                    </li>
                  </ul>
                </div>
                <app-button extraClass="btn view-project">
                  <a :href="projectInfo.url" target="_blank">View Project</a>
                </app-button>
              </div>
            </div>
          </div>
          <!------- End Portfolio Items --------->
        </div>
      </div>
    </section>

    <!-------------- PENDING DYNAMIC MODAL WHIT BOOTSTRAP -------------->
    <!------- Portfolio Item Details Popup ------->
    <div class="portfolio-popup">
      <div class="pp-inner">
        <div class="pp-content">
          <div class="pp-header">
            <button class="btn pp-close">
              <span class="material-icons"> close </span>
            </button>
            <div class="pp-thumbnail">
              <img src="@/assets/img/portfolio/3.jpg" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
    <!------- End Portfolio Item Details Popup ------->
    <!-------------- PENDING DYNAMIC MODAL WHIT BOOTSTRAP -------------->
  </div>
</template>

<script>
export default {
  name: "app-portfolio",
  data() {
    return {
      //REFACTOR WITH VUEX
      projectsInfo: [
        {
          id: 1,
          name: "Fire app",
          image: require("../assets/fire-app.png"),
          englishDescription:
            "Visualize centralized static data, consume external data, add own vue libraries, to create a simple fire extinguisher rental system.",
          spanishDescription:
            "Visualizar datos estáticos centralizados, consumir datos externos, agregar librerías propias de vue, para crear un sistema sencillo de renta de extintores.",
          createdAt: "March 2022",
          tecnologies:
            "HTML, CSS, Nuxt JS, Axios, Random user api and Continuous Deployment with Netlify",
          url: "https://fire-app.netlify.app/",
        },
        {
          id: 2,
          image: require("../assets/movie-app.png"),
          name: "Movie App",
          englishDescription:
            "You can search a specific movie that you want and see some information.",
          spanishDescription:
            "Puedes buscar una película específica que quieras y ver algunos detalles relacionados a ella.",
          createdAt: "December 2021",
          tecnologies: "HTML, CSS (responsive), Nuxt JS, Axios and TMDB API",
          url: "http://learning-with-movie-app.herokuapp.com/",
        },

        {
          id: 1,
          name: "My Portfolio",
          image: require("../assets/portfolio-home.png"),
          englishDescription:
            "You can search a specific movie that you want and see some information.",
          spanishDescription:
            "El espacio perfecto para conocer un poco más sobre mí y sobre mi trabajo.",
          createdAt: "January 2022",
          tecnologies: "HTML, CSS, VueJs, Vue Router",
          url: "https://lauravz-portfolio.netlify.app/",
        },
      ],
    };
  },
};
</script>

<style lang="scss"></style>
