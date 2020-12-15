<template>
  <div class="container" id="home">
      <CardNav />
      <h1>Otal</h1>
      <CardFil />
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
  width: 100%;

h1 {
  font-family: 'Montserrat', sans-serif;
  color: $black;
  font-weight: bold;
  font-size: 30px;
  text-align: center;
  margin: 20px 0;
}

}

</style>
