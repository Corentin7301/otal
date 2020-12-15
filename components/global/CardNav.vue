<template>
  <div class="card">
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
    &::-webkit-scrollbar {
      display: none;
    }


    img {
      margin-right: 10px;

    }
  }

</style>
