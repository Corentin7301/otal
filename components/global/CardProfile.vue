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
    font-family: 'Montserrat', sans-serif;
    font-weight: 400;
    color: $black;
    background-color: rgb(233, 233, 233);
    display: grid;
    grid-template-columns: repeat(3, 123px);
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

    .cards {
      margin-top: 32px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;

      .cardFil {
        background-color: rgb(233, 233, 233);
        display: grid;
        grid-template-columns: repeat(5, 224px);
        grid-gap: 15px;

        .content {
          height: 224px;
          background-color: white;
          border-radius: 7px;
          overflow: hidden;
        }
      }

    }
  }

</style>
