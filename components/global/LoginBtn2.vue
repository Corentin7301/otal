<template>
<div>
      <a
        :href="url"
        class="btn-login2">
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
.btn-login2 {
  font-family: 'Montserrat', sans-serif;
  font-weight: 500;
  color: #f4f4f9c9;
  background-color: $purple;
  text-decoration: inherit;
  font-size: 13px;
  padding: 5px 22px;
  border-radius: 24px;
  text-align: center;
}
</style>
