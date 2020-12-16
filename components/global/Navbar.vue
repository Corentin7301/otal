<template>
  <nav>
    <div class="mobile">
      <div class="spacer"></div>
      <nuxt-link to="/">
        <img src="@/assets/img/logo1.png" alt="logo">
      </nuxt-link>
      <nuxt-link to="/save">
        <img src="@/assets/img/save.svg" alt="save">
      </nuxt-link>
    </div>
    <div class="desktop">
      <nuxt-link to="/">
        <img src="@/assets/img/logo1.png" alt="logo">
      </nuxt-link>
      <nuxt-link to="/">Accueil</nuxt-link>
      <nuxt-link to="/explore" class="explore">Découvrir</nuxt-link>
      <input type="text" name="search" id="search" placeholder="Rechercher...">
      <LoginBtn url="/login">Se connecter</LoginBtn>
    </div>

  </nav>
</template>

<script>
  export default {
    name: 'Navbar',
    data() {
      return {

      }
    }
  }

</script>

<style lang="scss" scoped>
  .mobile {
    position: sticky;
    top: 0;
    margin-top: 30px;
    width: 100%;
    height: 65px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 17px;
    border-bottom: solid 1.5px $black;
    z-index: 1;
    background-color: white;

    img {
      height: 37px;
    }

    .spacer {
      width: 27px;
    }

  }

  .desktop {
    display: none;
  }

  @media screen and (min-width: 1280px) {

    .desktop {
      padding: 0 50px;
      font-family: 'Montserrat', sans-serif;
      font-weight: 500;
      font-size: 16px;
      display: flex;
      align-items: center;
      height: 80px;
      background-color: white;
      box-shadow: 0px 3px 6px #0000001F;

      img {
        height: 40px;
        margin-right: 43px;
      }

      .explore {
        margin: 0 200px 0 50px;
      }

      input {
        text-align: center;
        padding: 5px 90px;
        border: 2px solid #B1B1B1;
        border-radius: 24px;
        margin-right: 340px;
      }

      .nuxt-link-exact-active {
        font-weight: bold;
      }
    }


  .mobile {
    display: none;
  }
  }


</style>
