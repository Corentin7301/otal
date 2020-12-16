<template>
  <div id="postPage">
    <div v-for="post in posts" :key="post.id" class="cardPage">
      <div class="leftCardPage">
        <img :src="post.img" alt="post">
        <div class="footerLeft">
          <img :src="post.img_profil" alt="user">
          <h3>{{post.creator}}</h3>
        </div>
        <svg class="w-6 h-6 heart" fill="none" stroke="currentColor" viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z">
          </path>
        </svg>
        <svg class="w-6 h-6 upload" fill="none" stroke="currentColor" viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"></path>
        </svg>
        <svg class="w-6 h-6 savePost" fill="none" stroke="currentColor" viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M5 5a2 2 0 012-2h10a2 2 0 012 2v16l-7-3.5L5 21V5z"></path>
        </svg>
      </div>
      <div class="rightCardPage">
        <h4 class="medium">{{post.description}}</h4>
        <p class="bold">Commentaires :</p>
        <div v-for="comment in comments" :key="comment.id" class="commentaires">
          <img :src="comment.img_profil" alt="commentaire">
          <h4 class="bold">{{comment.creator}}</h4>
          <p>{{comment.commentaire}}</p>
        </div>
        <div class="footerRight">
          <h3 class="bold">{{post.creator}}</h3>
          <input type="text" name="commentaire" id="commentaire">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import posts from '@/data/posts.json';
  import comments from '@/data/comments.json';
  export default {
    data() {
      return {
        posts,
        comments
      }
    },
  }

</script>

<style lang="scss">
  #postPage {
    width: 100%;
    font-family: 'Montserrat', sans-serif;

    .cardPage {
      display: flex;
      //   align-items: center;
      justify-content: space-between;
      margin: 85px 95px 50px 50px;



      .leftCardPage {
        width: 550px;
        height: 550px;
        border-radius: 7px;
        overflow: hidden;
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-right: 100px;

        img {
          height: 100%;
        }

        svg {
          width: 30px;
          color: $purple;
        }

        .heart {
          position: absolute;
          top: 15px;
          right: 10px;
        }

        .upload {
          position: absolute;
          top: 60px;
          right: 10px;
        }

        .savePost {
          position: absolute;
          top: 105px;
          right: 10px;
        }

        .footerLeft {
            height: 62px;

          img {
              width: 45px;
            height: 45px;
            border-radius: 50%;
              
          }
        }
      }



      .rightCardPage {
        display: flex;
        flex-direction: column;

        h4 {
          color: $black;
          width: 520px;
          margin: 0 65px 28px 0;
          font-size: 16px;
        }

        p {
          color: $grey;
          font-size: 16px;
          margin-bottom: 45px;
        }

        .commentaires {
          display: flex;
          align-items: center;
          margin-bottom: 20px;

          img {
            width: 45px;
            height: 45px;
            border-radius: 50px;
            border: 4px solid $purple;
            margin-right: 5px;
          }

          h4 {
            margin: 0;
            width: 200px;
            color: #16192580;
            font-size: 15px;
          }

          p {
            margin: 0;
            width: 336px;
          }
        }
      }

      .footerRight {
        display: flex;
        align-items: center;
        h3 {
          color: #16192580;
          font-size: 15px;
        }

        input {
          font-size: 15px;
          color: $grey;
          font-weight: 500;
          padding: 5px 14px;
          border: 2px solid #B1B1B1;
          border-radius: 24px;
          margin-right: 0;
          width: 230px;
          margin-left: 100px;
        }
      }
    }
  }

</style>
