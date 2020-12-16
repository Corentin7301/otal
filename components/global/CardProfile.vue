<template>
  <div class="cards">

    <div class="cardFil">
      <div v-for="post in posts" :key="post.id" class="content">
        <div class="post">
          <img :src="post.img" alt="post">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import posts from '@/data/posts.json';
  export default {
    data() {
      return {
        posts
      }
    }
  }

</script>

<style lang="scss" scoped>
  .cardFil {
    padding: 0 5px;
    font-family: 'Montserrat', sans-serif;
    font-weight: 400;
    color: $black;
    background-color: rgb(233, 233, 233);
    display: grid;
    grid-template-columns: repeat(3, 33%);
    grid-gap: 3px;

    .post {
      overflow: hidden;
      height: 123px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    img {
      height: 100%;
    }
  }

  @media screen and (min-width: 1280px) {


      .cardFil {
        background-color: rgb(233, 233, 233);
        display: grid;
        grid-template-columns: repeat(5, 19%);
        grid-gap: 15px;
        justify-content: center;

        .post {
          overflow: hidden;
          height: 224px;
          display: flex;
          align-items: center;
          justify-content: center;
        }

        img {
          height: 100%;
        }
      }

    }

</style>
