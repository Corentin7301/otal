<template>
  <div id="footer">
      <nuxt-link to="/" class="menu"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"></path></svg></nuxt-link>
      <nuxt-link to="/explore" class="menu"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path></svg></nuxt-link>
      <nuxt-link to="/add" class="menu"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v3m0 0v3m0-3h3m-3 0H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg></nuxt-link>
      <nuxt-link to="/notifs" class="menu"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"></path></svg></nuxt-link>
      <nuxt-link to="/profile" class="menu"><img src="~/assets/img/profile.jpg" alt="profil"></nuxt-link>
    </div>
</template>

<script>
  export default {
    name: "footer",
    data() {
      return {

      };
    },
  };

</script>

<style lang="scss" scoped>
  #footer {
    position: sticky;
    bottom: 0;
    height: 63px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    border-top: solid 1.5px $black;
    padding-top: 20px;

    svg {
      width: 35px;
      color: #B1B1B1;
      margin-bottom: 20px;
    }

    img {
      width: 35px;
      border-radius: 50px;
      margin-bottom: 20px;
    }
  }

</style>
