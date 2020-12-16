<template>
  <div class="container" id="login">
    <div class="leftLogin">
      <h1 class="medium">Créer un compte</h1>
      <LoginBtn2 url="#" class="googleLogin">Se connecter avec Google</LoginBtn2>
      <p>Ou</p>
      <div class="inputCreateProfil">
        <div id="name">
          <input type="text" name="nom" id="nom" placeholder="Nom">
          <input type="text" name="prenom" id="prenom" placeholder="Prénom">
        </div>
        <input type="email" name="email" id="email" placeholder="Adresse E-mail">
        <input type="password" name="password" id="password" placeholder="Mot de passe">
      </div>
      <div class="LoginLogout">
        <nuxt-link to="/">
          <LoginBtn2 url="/" class="login">Créer</LoginBtn2>
        </nuxt-link>
        <nuxt-link to="/login"><button class="create">Se connecter</button></nuxt-link>
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

      .inputCreateProfil {
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
          margin-bottom: 28px;

        }
      }

      #name {
        display: flex;
        align-items: center;

        input {
          width: 180px;
          margin-right: 20px;
        }
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
