<template>
    <ul id="social" :class="displayShow">
      <social-network url="http://www.instagram.com">
        <i class="fab fa-instagram"></i>
      </social-network>
      <social-network url="http://www.twitter.com">
        <i class="fab fa-twitter"></i>
      </social-network>
      <social-network url="http://www.facebook.com">
        <i class="fab fa-facebook"></i>
      </social-network>
      <social-network url="http://www.linkedin.com">
        <i class="fab fa-linkedin"></i>
      </social-network>
    </ul>
</template>

<script>
export default {
  name: "socialShare",
  props: ['display'],
  data() {
    return {
      scrollY:0,
      // will be hide after 350 px scroll down
      hideFrom: 350
      }
  },
  methods: {
    setScrollY(){
      this.scrollY = window.scrollY;
    }
  },
  computed: {
    // inline || fixed || none
    displayShow(){
      if (this.display === 'inline') {
        return "inline"
      } 
      if ( this.display === "fixed") {
        if ( this.scrollY > this.hideFrom ){
          return "none"
        } else
        { return "fixed" }
      }

    }
  },
  mounted() {
    window.addEventListener('scroll', (event) => {
      this.setScrollY()
    })
  }
}
</script>

<style lang="scss" scoped>

.fixed {
  position: fixed;
  right: 50px;
  top: 50%;
  z-index: 1;
}

.inline {
  display: flex;
}

.none {
  display: none;
}

</style>
