<template>
  <div class="container" id="login">
    <div class="leftLogin">
      <h1 class="medium">Se connecter</h1>
      <LoginBtn2 url="#" class="googleLogin">Se connecter avec Google</LoginBtn2>
      <p>Ou</p>
      <div class="inputLogin">
        <input type="email" name="email" id="email" placeholder="Adresse E-mail">
        <input type="password" name="password" id="password" placeholder="Mot de passe">
      </div>
      <p class="forget medium">J'ai oublié mon mot de passe</p>
      <div class="LoginLogout">
        <nuxt-link to="/">
          <LoginBtn2 url="#" class="login">Se connecter</LoginBtn2>
        </nuxt-link>
        <nuxt-link to="/CreateProfil"><button class="create">Créer un compte</button></nuxt-link>
      </div>
    </div>
    <div class="rightLogin">
      <img src="~/assets/img/otal.png" alt="otal">
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

<style lang="scss">
  #login {
    width: 100%;
    height: 100%;
    font-family: 'Montserrat', sans-serif;
    display: flex;
    padding-left: 100px;

    .leftLogin {
      width: 50%;

      h1 {
        color: $black;
        margin: 83px 0 38px 0;
      }

      .googleLogin {
        margin-bottom: 16px;
      }

      p {
        margin-bottom: 14px;
      }

      .inputLogin {
        display: flex;
        flex-direction: column;

        input {
          font-size: 15px;
          color: $grey;
          font-weight: 500;
          padding: 5px 14px;
          border: 2px solid $grey2;
          border-radius: 24px;
          width: 380px;
        }
      }

      #email {
        margin-bottom: 28px;
      }

      #password {
        margin-bottom: 16px;
      }

      .forget {
        text-align: right;
        width: 380px;
        font-size: 11px;
        color: $grey2;
        margin-bottom: 16px;
      }


      .LoginLogout {
        display: flex;
        align-items: center;

        button {
          border: 2px solid $purple;
          border-radius: 25px;
          padding: 4px 18px;
          color: #3C3C3B;
          font-family: 'Montserrat', sans-serif;
          font-size: 13px;
          margin-left: 14px;
          cursor: pointer;
        }
      }
    }

    .rightLogin {
      width: 50%;
      display: flex;
      justify-content: right;
    }
  }

</style>
