<template>
  <nav>
    <div class="spacer"></div>
    <nuxt-link to="/">
      <img src="@/assets/img/logo1.svg" alt="logo">
    </nuxt-link>
    <nuxt-link to="/save">
      <img src="@/assets/img/save.svg" alt="save">
    </nuxt-link>

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
    background-color: white;
    margin-top: 30px;
    width: 100%;
    height: 65px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 17px;
    border-bottom: solid 1.5px $black;
    position: sticky;
    top: 0;

    img {
      height: 37px;
    }

    .spacer {
      width: 27px;
    }

  }

</style>
