<template>
<div>
      <a
        :href="url"
        class="btnExplore">
        <slot/>
      </a>
</div>
</template>

<script>

export default {
  name: "",
  // components:{Name},
  props: ['url'],
  data() {
      return {
        
      }
  },
}
</script>

<style lang="scss" scoped>
.btnExplore {
  background-color: $grey;
  font-family: 'Montserrat', sans-serif;
  font-weight: 500;
  color: white;
  text-decoration: inherit;
  font-size: 10px;
  padding: 4px 8px;
  border-radius: 24px;
  border: 2px solid $grey2;
  text-align: center;
}
</style>
