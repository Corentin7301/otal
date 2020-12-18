<template>
  <div>

    <div class="mobileHeaderProfil">
      <div class="headerReseau">
        <div class="headprofil">
          <div class="barreReseaux">
            <img src="~/assets/img/user.jpg" alt="utilisateur">
            <h3>Bastien Manent</h3>
            <a href="https://www.instagram.com/" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="https://twitter.com" target="_blank"><i class="fab fa-twitter"></i></a>
            <a href="https://fr.linkedin.com/" target="_blank"><i class="fab fa-linkedin"></i></a>
          </div>
          <p class="bio">Plus besoin de me présenter, tous le monde me connait, mais vous pouvez me suivre sur mes
            réseaux
            si ce n'est
            pas encore fait.</p>
          <div class="barreStats">
            <button>S'abonner</button>
            <p class="medium"></p>
            <p><span class="medium">120 </span>Abonnés</p>
            <p><span class="medium">14 </span>Projets</p>
            <p><span class="medium">258 </span>j'aime</p>
          </div>
        </div>
      </div>
    </div>
    <div class="desktopHeaderProfil">
      <div class="headerReseau">
        <div class="headprofil">
          <img src="~/assets/img/user.jpg" alt="utilisateur">
          <div class="barreBody">
            <div class="barreText">
              <h3>Bastien Manent</h3>
              <p class="bio">Plus besoin de me présenter, tous le monde me connait, mais vous pouvez me suivre sur mes
                réseaux
                si ce n'est
                pas encore fait.</p>

            </div>
            <div class="barreStats">
              <button>S'abonner</button>
              <p class="medium"></p>
              <p><span class="medium">120 </span>Abonnés</p>
              <p><span class="medium">14 </span>Projets</p>
              <p><span class="medium">258 </span>j'aime</p>
            </div>
          </div>
          <div class="barreReseaux">
            <nuxt-link to="https://www.instagram.com/"><i class="fab fa-instagram"></i></nuxt-link>
            <nuxt-link to="https://twitter.com/"><i class="fab fa-twitter"></i></nuxt-link>
            <nuxt-link to="https://fr.linkedin.com/"><i class="fab fa-linkedin"></i></nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {

      }
    },
  }

</script>

<style lang="scss" scoped>
  .headprofil {
    padding: 0 16px;
    box-shadow: 0px 2px 10px #00000029;
    margin-bottom: 25px;

    .barreReseaux {
      padding-top: 12px;
      display: flex;
      align-items: center;

      img {
        width: 40px;
        margin: 0 10px 11px 0;
        border-radius: 50px;
        border: 4px
      }

      h3 {
        width: 250px;
        font-size: 15px;
      }

      i {
        width: 14px;
        margin-right: 16px;
      }
    }

    .bio {
      width: 276px;
      margin-bottom: 5px;
    }

    .barreStats {
      display: flex;
      align-items: center;
      margin-top: 22px;
      padding-bottom: 22px;

      button {
        background-color: $purple;
        border: none;
        border-radius: 25px;
        padding: 5px 24px;
        color: white;
        font-family: 'Montserrat', sans-serif;
        font-size: 13px;
      }

      p {
        font-size: 12px;
        margin-right: 8px;
      }

    }
  }

  .desktopHeaderProfil {
    display: none;
  }

  @media screen and (min-width: 1280px) {
    .desktopHeaderProfil {
      display: block;
      color: $black;

      .headprofil {
        display: flex;

        img {
          width: 100px;
          height: 100px;
         
          border-radius: 50px;
          border: 4px solid $purple;
        margin: 30px 60px 0 30px;
        }

        .barreBody {
        margin: 30px 0;
          display: flex;
          flex-direction: column;
        margin-right: 135px;

          .barreText {
              display: flex;
              align-items: center;
              

              h3 {
                  font-size: 25px;
                  margin-right: 32px;
              }

              p{
                  height: 38px;
                  width: 600px;
                  font-size: 16px;
              }
          }
          .barreStats {

              button {
                  padding: 9px 38px;
                  margin-right: 90px;
              }

              p {
                  font-size: 14px;
              }
          }
        }
        .barreReseaux {
           height: 40px;
           padding: 0;
           margin-top: 30px;
            i {
                font-size: 26px;
                margin-right: 30px;
            }
        }
      }






    }









    .mobileHeaderProfil {
      display: none;
    }
  }

</style>
