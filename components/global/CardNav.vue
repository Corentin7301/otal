<template>
  <div class="card scroll-color-colors scroll-width-thin">
    <img src="~/assets/img/ui_ux_design.png" alt="ui-ux-design">
    <img src="~/assets/img/illustration.png" alt="illustration">
    <img src="~/assets/img/graphisme.png" alt="graphisme">
    <img src="~/assets/img/dev.png" alt="developpement">
    <img src="~/assets/img/photo.png" alt="photo">
    <img src="~/assets/img/video.png" alt="video">
    <img src="~/assets/img/audio.png" alt="audio">
  </div>
</template>

<script>
  export default {
    name: "card",
    data() {
      return {

      }
    },
  }

</script>

<style lang="scss" scoped>

  .card {
    display: flex;
    align-items: center;
    margin-top: 15px;
    width: 100%;
    overflow-x: scroll;
    overflow-y: hidden;
    &::-webkit-scrollbar { /* Chrome */
      display: none;
    }
    scrollbar-width: none; /* Firefox 64 */
    -ms-overflow-style: none; /* IE 11 */

    img {
      margin-right: 10px;

    }
  }

    @media screen and (min-width: 1280px) {
      .card {
        &::-webkit-scrollbar { /* Chrome */
          display: inherit;
        }
        scrollbar-width: inherit; /* Firefox 64 */
        -ms-overflow-style: inherit; /* IE 11 */
      }

    }

</style>
