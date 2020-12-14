<template>
  <div id="footer">
    <div class="footer-col">
    <nuxt-link
      v-for="item in items" 
      :key="item.name"
      :to="item.page"
      class="button"
    >{{item.name}}</nuxt-link>
    </div>
    <div class="footer-col">
   
        <social-share display="inline" />
    </div>
  </div>
</template>

<script>
export default {
  name: "footer",
  data() {
    return {
      items: [
          {name: 'Accueil', page: '/'},
          {name: 'A propos', page: '/about'},
          {name: 'Contact', page: '/contact'}
        ]
    };
  },
};
</script>

<style lang="scss" scoped>
#footer {
  height: 300px;
  background: $coolGrad;
  display: flex;
  justify-content: center;
  align-items: center;
  .footer-col {
    flex: 0 1 400px;
    display: flex;
    flex-direction: column;
    a,
    p {
      font-size: 30px;
      color: white;
      text-decoration: inherit;
      font-family: "HelveticaNeue";
      &:hover {
        font-weight: bold;
      }
    }
  }
}

.news {
  background-color: white;
  padding: 40px;
  border-radius: 8px;
}

.form-cta {
  color: white;
  background: $coolGrad;
  border: none;
  padding: 8px 12px;
}

.footer-social {
  display: flex;
}
</style>
