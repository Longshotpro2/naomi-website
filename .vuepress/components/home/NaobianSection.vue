<template>
  <div class="naobian-section">
    <div class="naobian-container">
      <ClientOnly>
        <parallax :speed-factor="0.15">
          <img src="./images/rpi.jpg" alt="raspberry pi" style="filter: brightness(75%);">
        </parallax>
      </ClientOnly>
      <div class="naobian-text">
        <h2 class="slide-seq">Set up your own Naomi system in just a few steps</h2>
        <p class="slide-seq">
          Try the provided hassle-free Naobian image for the Raspberry Pi, a widely used and recommended hardware choice.
          Flash an SD card, boot, and enjoy your up-to-date Naomi setup with conveniently pre-configured system settings and software.
        </p>
        <router-link to="dev/docs/installation/naobian.html" class="learn-how-button slide-seq">Learn How ➜</router-link>
      </div>
    </div>
  </div>
</template>


<style lang="stylus">
.naobian-section
  height 70vh
  background black
  color white
  display flex
  font-family 'Open Sans', sans-serif
  font-weight normal
  overflow hidden
  .naobian-container
    position relative
    height 70vh
    width 100%
    overflow: hidden
  .Masthead
    width 100%
    z-index 10 !important
    .Masthead__image
      // height 300px !important
  .naobian-text
    position absolute
    width 100%
    top 0
    text-align center
    z-index 12
    h2
      font-size 2.5em
      font-weight 300
      border none
    p
      margin 1rem
    .learn-how-button
      display inline-block
      font-size 1rem
      color #fff
      padding 0.8rem 1.6rem
      border-radius 4px
      background-color rgba(0, 0, 0, 0.3)
      transition background-color .1s ease
      box-sizing border-box
      border 1px solid #fff
      &:hover
        background-color #fff
        color black
      
  @media (max-width: 768px)
    &
      height 550px
    .naobian-container
      height 550px
    .Masthead
      height 550px !important
      .Masthead__image > img
        opacity 0.6

</style>

<script>
import parallax from 'vue-parallaxy'

export default {
  components: {
    parallax
  }  
}
</script>
