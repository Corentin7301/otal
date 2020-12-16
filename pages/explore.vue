<template>
  <div class="container" id="explore">
    <div class="search">
      <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
          d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
      </svg>
      <input type="text" name="searchExplore" id="searchExplore" class="medium" placeholder="Rechercher...">
    </div>
    <HeaderExplore />
    <CardDesktop />
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
  #explore {
    width: 100%;

    .search {
      height: 58px;
      background-color: white;
      display: flex;
      align-items: center;
      border-bottom: solid 1.5px #16192536;

      svg {
        width: 27px;
        color: $grey;
        margin: 0 17px 0 16px;
      }

      input {
        font-family: 'Montserrat', sans-serif;
        border: none;
        font-size: 15px;
        color: $grey;

        &:focus {
          outline: none;
        }
      }

    }

  }

</style>
