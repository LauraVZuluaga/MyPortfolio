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
          <!-------------- PENDING REFACTORING WITH A COMPONENT -------------->
          <!------- Portfolio Items --------->
          <div class="portfolio-item">
            <div class="portfolio-item-thumbnail">
              <img
                src="@/assets/portfolio-home.png"
                alt="portfolio item thumb"
              />
            </div>
            <h3 class="portfolio-item-title">My Portfolio</h3>
            <div class="portfolio-item-details">
              <div class="pp-body">
                <div class="description">
                  <p>
                    The perfect space to get to know a little more about me and
                    about my work.
                  </p>
                  <br />
                  <p>
                    El espacio perfecto para conocer un poco más sobre mí y
                    sobre mi trabajo.
                  </p>
                </div>
                <div class="general-info">
                  <ul>
                    <li>Created - <span> January 2022 </span></li>
                    <li>Tecnologies used - <span> HTML, CSS, VueJs </span></li>
                    <!-- <li>Objetive - <span> HTML, CSS... </span></li>
                    <li>
                      View online -
                      <span>
                        <a href="#" target="_blank">www.algunacosa.com</a>
                      </span>
                    </li> -->
                  </ul>
                </div>
                <app-button extraClass="btn view-project">
                  <a
                    href="https://lauravz-portfolio.netlify.app/"
                    target="_blank"
                    >View Project</a
                  >
                </app-button>
              </div>
            </div>
          </div>
          <!------- End Portfolio Items --------->

          <!------- Portfolio Items --------->
          <div class="portfolio-item">
            <div class="portfolio-item-thumbnail">
              <img src="@/assets/movie-app.png" alt="portfolio item thumb" />
            </div>
            <h3 class="portfolio-item-title">Movie App</h3>
            <div class="portfolio-item-details">
              <div class="pp-body">
                <div class="description">
                  <p>
                    You can search a specific movie that you want and see some
                    information.
                  </p>
                  <br />
                  <p>
                    Puedes buscar una película específica que quieras y ver
                    algunos detalles relacionados a ella.
                  </p>
                </div>
                <div class="general-info">
                  <ul>
                    <li>Created - <span> December 2021 </span></li>
                    <li>
                      Tecnologies used -
                      <span> HTML, CSS, Nuxt JS and TMDB API </span>
                    </li>
                    <!-- <li>Objetive - <span> HTML, CSS... </span></li>
                    <li>
                      View online -
                      <span>
                        <a href="#" target="_blank">www.algunacosa.com</a>
                      </span>
                    </li> -->
                  </ul>
                </div>
                <app-button extraClass="btn view-project">
                  <a
                    href="http://learning-with-movie-app.herokuapp.com/"
                    target="_blank"
                    >View Project</a
                  >
                </app-button>
              </div>
            </div>
          </div>
          <!------- End Portfolio Items --------->

          <!------- Portfolio Items --------->
          <div class="portfolio-item">
            <div class="portfolio-item-thumbnail">
              <img src="@/assets/rent-app(2).png" alt="portfolio item thumb" />
            </div>
            <h3 class="portfolio-item-title">Rent App</h3>
            <div class="portfolio-item-details">
              <div class="pp-body">
                <div class="description">
                  <p>
                    Project to practice responsive designs. Right now it's
                    visual only, soon integration with Firebase to make it
                    dynamic.
                  </p>
                  <br />
                  <p>
                    Proyecto para practicar diseños responsivos. Ahora mismo es
                    sólo visual, pronto, integración con Firebase para hacerlo
                    dinámico.
                  </p>
                </div>
                <div class="general-info">
                  <ul>
                    <li>Created - <span> October 2021 </span></li>
                    <li>
                      Tecnologies used -
                      <span>
                        HTML, CSS, VueJs, PWA, Babel, Router, Vuex and Less.
                      </span>
                    </li>
                    <!-- <li>Objetive - <span> HTML, CSS... </span></li>
                    <li>
                      View online -
                      <span>
                        <a href="#" target="_blank">www.algunacosa.com</a>
                      </span>
                    </li> -->
                  </ul>
                </div>
                <app-button extraClass="btn view-project">
                  View Project
                </app-button>
              </div>
            </div>
          </div>
          <!------- End Portfolio Items --------->
          <!-------------- PENDING REFACTORING WITH A COMPONENT -------------->
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
};
</script>

<style lang="scss"></style>
