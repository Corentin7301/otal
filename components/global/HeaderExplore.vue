<template>
  <div class="explore">
    <h1 class="medium">Découvrir</h1>
    <ExploreBtn url="#">Développement</ExploreBtn>
    <ExploreBtn url="#">UX design</ExploreBtn>
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
  .explore {
    display: flex;
    align-items: center;
    padding: 14px 0;

    h1 {
      font-family: 'Montserrat', sans-serif;
      color: #B8B9BD;
      font-size: 25px;
      margin: 0 30px 0 14px;
    }
  }

</style>
