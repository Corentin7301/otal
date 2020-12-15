<template>
  <div class="container" id="">
      <!-- Header Profil -->
    <div class="headerReseau">
      <div class="headProfil">
        <div class="barreReseaux">
          <img src="~/assets/img/user.png" alt="utilisateur">
          <h3>Bastien Manent</h3>
          <i class="fab fa-instagram"></i>
          <i class="fab fa-twitter"></i>
          <i class="fab fa-linkedin"></i>
        </div>
        <p class="bio">Plus besoin de me présenter, tous le monde me connait, mais vous pouvez me suivre sur mes réseaux
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
      <!-- /Header Profil -->
      <CardProfile />
  </div>
</template>
<script>
  export default {
    data() {
      return {

      }
    }
  }

</script>


<style lang="scss" scoped>
  .container {
    width: 100%;
    font-family: 'Montserrat', sans-serif;

    .headProfil {
      padding: 0 16px;
      box-shadow: 0px 2px 10px #00000029;
      margin-bottom: 25px;

      .barreReseaux {
        margin-top: 12px;
        display: flex;
        align-items: center;

        img {
          width: 40px;
          margin: 0 10px 11px 0;
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
  }

</style>
