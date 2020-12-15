<template>
  <div class="container" id="home">
    <CardNav class="CardNav" />
    <h1>Otal</h1>
    <HeaderDesktop class="HeaderDesktop" />
    <CardFil />
    <nuxt-link to="#">
      <svg id="cercle" class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"
        xmlns="http://www.w3.org/2000/svg">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
          d="M12 9v3m0 0v3m0-3h3m-3 0H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"></path>
      </svg>
    </nuxt-link>
  </div>
</template>

<script>
  export default {
    name: "",
    head() {
      return {
        //  string or this.XXXX
        titre: "my home",
        meta: [{
          hid: 'description',
          name: 'description',
          content: 'My home description '
        }]
      }
    }
  }

</script>


<style lang="scss">
  #home {
    width: 100%;

    h1 {
      font-family: 'Montserrat', sans-serif;
      color: $black;
      font-weight: bold;
      font-size: 30px;
      text-align: center;
      margin: 20px 0;
    }

    .HeaderDesktop {
      display: none;
    }

    #cercle {
      display: none;
    }
  }

  @media screen and (min-width: 1280px) {

    #home {
      .HeaderDesktop {
        display: flex;
      }

      width: 100%;

      h1 {
        display: none;
      }

      .CardNav {
        display: none;
      }

      #cercle {
        display: block;
        color: #ca84f3;
        position: fixed;
        bottom: 30px;
        right: 30px;
        width: 50px;
        z-index: 1;
      }
    }
  }

</style>
