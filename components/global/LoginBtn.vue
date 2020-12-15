<template>
<div>
      <a
        :href="url"
        class="btn-login">
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
.btn-login {
  font-family: 'Montserrat', sans-serif;
  font-weight: 500;
  color: $black;
  text-decoration: inherit;
  font-size: 16px;
  padding: 4px 8px;
  border-radius: 24px;
  border: 2px solid #B1B1B1;
  text-align: center;
}
</style>
