<template>
  <nav>
    <div class="mobileNav">
      <div class="spacer"></div>
      <nuxt-link to="/">
        <img src="@/assets/img/logo1.png" alt="logo">
      </nuxt-link>
      <nuxt-link to="#">
        <img src="@/assets/img/save.svg" alt="save">
      </nuxt-link>
    </div>
    <div class="desktopNav">
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
  nav {
    position: sticky;
    top: 0;
    z-index: 1;

    .mobileNav {
      margin-top: 30px;
      width: 100%;
      height: 65px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 17px;
      border-bottom: solid 1.5px #1619255d;
      background-color: white;

      img {
        height: 37px;
      }

      .spacer {
        width: 27px;
      }

    }

    .desktopNav {
      display: none;
    }
  }

  @media screen and (min-width: 1280px) {
    nav {

      .desktopNav {
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
          border: 2px solid $grey2;
          border-radius: 24px;
          margin-right: 340px;
        }

        .nuxt-link-exact-active {
          font-weight: bold;
        }
      }


      .mobileNav {
        display: none;
      }
    }
  }

</style>
