<template>
  <div>
    <div class="text">
      <h2 class="world bold">Découvrir</h2>
      <h2 class="otal">Le meilleur de <span class="bold">Otal</span></h2>
    </div>
    <CardNav class="CardNavbar"/>
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
  div {
    background-color: white;
    align-items: center;
    box-shadow: 0px 3px 6px #0000001F;

    h2 {
        display: block;
      font-family: 'Montserrat', sans-serif;
      color: $black;
      font-weight: 500;
      font-size: 30px;
      margin: 0;
    }

    .text {
        width: 800px;
        margin: 0 450px 0 50px;
        box-shadow: none;
      .world {
        font-size: 30px;
      }

      .otal {
        font-size: 20px;
      }
    }
    .CardNavbar {
        margin: 30px 0 30px 0;
    }
  }

</style>
