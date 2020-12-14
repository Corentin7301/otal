<template>
  <div class="container" id="home">
      PAGE ACCUEIL
  </div>
</template>

<script>
export default {
  name: "",
  head() {
      return {
        //  string or this.XXXX
        titre: "my home",
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: 'My home description '
          }
        ]
      }
    }
}
</script>


<style lang="scss">
#home {
  height: 700px;
  display: flex;
  justify-content: center;
  align-items: center;
}

</style>
