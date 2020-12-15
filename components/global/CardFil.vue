<template>
  <div class="cards">

    <div class="cardFil">
      <div v-for="post in posts" :key="post.id" class="content">
        <img src="~/assets/img/saveIcon.svg" alt="save" class="save">
        <img :src="post.img" alt="post">
        <div class="Cardbar">
          <img :src="post.img_profil" :alt="post.creator" class="creator">
          <h3>{{post.creator}}</h3>
          <div class="like_comment">
            <i class="fas fa-heart"></i>
            <p>{{post.like}}</p>
            <i class="fas fa-comment"></i>
            <p>{{post.comment}}</p>
          </div>
        </div>
        <h4>{{post.description}}</h4>
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

    .content {
      position: relative;

    }

    img {
      width: 100%;
    }

    .save {
      position: absolute;
      right: 20px;
      top: -10px;
      width: 25px;
    }

    .Cardbar {
      display: flex;
      align-items: center;
      margin-top: 10px;
      padding: 0 16px;
      position: relative;

      .creator {
        width: 30px;
        height: 30px;
        border-radius: 50%;
        margin-right: 6px;
      }

      h3 {
        font-family: 'Montserrat', sans-serif;
        font-weight: 500;
        font-size: 15px;
      }

      .like_comment {
        position: absolute;
        right: 20px;
        display: flex;

        i {
          width: 14px;
          height: 14px;
          color: #3C3C3BB3;
          margin: 0 8px 0 16px;
        }

        p {
          font-size: 15px;
        }
      }
    }

    h4 {
      padding: 16px;
      font-size: 13px;
      color: $black;
      font-weight: 500;
      margin-bottom: 25px;
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
